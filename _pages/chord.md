---
permalink: /chord.html
title: "CHORD | On-device Personalized Recommendation"
excerpt: "Personalized on-device recommendation through device-cloud collaborative mixed-precision quantization."
author_profile: true
---

<a href="/" target="_self">← Back to homepage</a>

# CHORD

**Customizing Hybrid-precision On-device Model for Sequential Recommendation with Device-cloud Collaboration**  
*ACM Multimedia 2025* · [Paper (PDF)](https://www.arxiv.org/pdf/2510.03038) · [ACM Digital Library](https://dl.acm.org/doi/abs/10.1145/3746027.3755632)

CHORD gives each user a personalized recommendation model that runs on their device without training or fine-tuning a separate model for every user. It treats personalization as a **quantization problem**: devices share the same frozen weights, while each user gets a compact, customized mixed-precision strategy.

## The challenge: customization and compression together

On-device recommendation can reduce latency, protect user data, and ease server load. Making the model personal is harder: fine-tuning on each device requires backpropagation, while sending a fresh model to every user consumes bandwidth. Three sources of variation make the problem more demanding:

- **Different interests and devices.** Users have different tastes, and their devices have different memory, compute, and bandwidth budgets.
- **Changing interests.** A user's behavior can drift, making a one-time deployment stale.
- **Frequent model updates.** Transmitting updated weights to many devices is expensive.

CHORD addresses the coupled need to customize a model for each user and compress it for the user's device, while keeping device-cloud communication small.

## The idea: a per-user quantization strategy

The shared backbone stays frozen. Personalization lives in a **per-user, per-channel bit-width assignment**: sensitive channels keep higher precision and less sensitive channels use fewer bits. The cloud finds this quantization “lottery ticket”; the device applies it without training.

<a href="/images/chord-overview.png" target="_blank" aria-label="Open the full-size CHORD method figure"><img src="/images/chord-overview.png" alt="CHORD overview: on-device interest profiling, cloud-side sensitivity estimation, channel-wise mixed-precision strategy generation, and adaptation with frozen weights" width="100%"></a>

The strategy is generated in three stages:

1. **User profiling.** Recent interactions on the device produce latent interest embeddings that capture the user's current preferences.
2. **Multi-granularity sensitivity estimation.** Cloud-side hypernetworks estimate element-, filter-, and layer-level parameter importance. Element-level signals reconstruct filter importance, which is then weighted by layer-level importance.
3. **Personalized strategy generation.** The combined importance determines each channel's precision. Only the encoded strategy is transmitted; the device decodes and applies it according to its resource budget.

## Why it is efficient

- **Personalized recommendation:** each user receives a different precision pattern over the shared model.
- **Fast adaptation:** the device applies the strategy in a single forward pass, without on-device backpropagation.
- **Efficient inference:** importance-aware mixed precision yields a model with roughly **3-bit average precision**.
- **Lightweight transmission:** the strategy takes **2 bits per channel**, instead of sending full 32-bit weights.

## Experiments

CHORD is evaluated on three real-world datasets—**Amazon-CD, Yelp, and MovieLens-100K**—with two sequential-recommendation backbones, **SASRec** and **Caser**. The paper reports **NDCG@5/10** and **HR@5/10** against full-precision and compressed baselines. It finds higher recommendation quality, faster adaptation and inference, and lower transmission overhead.

Further experiments examine tighter resource budgets, different average bit-widths, weight–activation quantization, and training stability. Visualizations show that parameter importance varies across both layers and channels, motivating a strategy tailored to each user.

## Takeaway

CHORD personalizes the *precision assigned to channels* instead of repeatedly training or distributing personalized weights. Shared frozen weights, a compact channel-wise strategy, and one forward pass let a recommendation model adapt to users and resource-constrained devices with a small device-cloud exchange.

[Read the paper (PDF)](https://www.arxiv.org/pdf/2510.03038)
