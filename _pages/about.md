---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

My name is **Tianqi Liu (zh: 刘天琦)**. I am currently a first-year MS student in Zhejiang University, under the supervision of Prof.[Shengyu Zhang](https://person.zju.edu.cn/shengyuzhang).

My research interests primarily focus on **recommender systems** and **LLM agents**, particularly in **model customization, lightweight deployment, and reinforcement-learning-based refinement**. Recently, I have developed a growing interest in **personalized, user-centric LLM agents**, seeking to tackle the challenges of proactive interaction in human-agent interaction. 

# 🔥 News
- *2026.04*: &nbsp;🎉🎉 One paper has been accepted to ACL 2026.
- *2025.10*: &nbsp;🥳🥳 I went to Dublin, Ireland, to deliver an oral presentation of our paper CHORD in ACM MM 2025.
- *2025.07*: &nbsp;🎉🎉 One first-author paper has been accepted to ACM MM 2025.

  
# 📝 Publications

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">MM 2025</div><img src='../images/CHORD.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">
  
[CHORD: Customizing Hybrid-precision On-device Model for Sequential Recommendation with Device-cloud Collaboration](https://www.arxiv.org/pdf/2510.03038)

**Tianqi Liu**, Kairui Fu, Shengyu Zhang, Wenyan Fan, Zhaocheng Du, Jieming Zhu, Fan Wu, Fei Wu

- A framework for device-cloud collaborative personalized mixed-precision quantization that achieves model customization and compression with one forward pass.
- Frozen weights + Channel-wise quantization strategy  = Fast AND Personalized model adaptation.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ACL 2026</div><img src='../image.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[What’s Missing in Screen-to-Action? Towards a UI-in-the-Loop Paradigm for Multimodal GUI Reasoning](https://www.arxiv.org/pdf/2604.06995)

Songze Li, Xiaoke Guo, **Tianqi Liu**, Biao Yi, Zhaoyan Gong, Zhiqiang Liu, Huajun Chen, Wen Zhang

[Project](https://github.com/zjukg/UILoop)

- A GUI reasoning framework utilizing a 'Screen-UI Elements-Action' loop to achieve interpretable decision-making and precise interface parsing.
- UI-Driven RL (localization + semantics + utilization) + 26K UI-Comprehension Benchmark = Transparent multi-step GUI automation.
</div>
</div>



# 💡 Projects

<div style="display: flex; flex-wrap: wrap; gap: 16px; margin: 1em 0 2em 0; width: 100%;">
  <div style="flex: 1 1 280px; min-width: 260px; border: 1px solid #e4e2e2; border-radius: 6px; padding: 18px 20px; display: flex; flex-direction: column;">
    <a href="https://github.com/mrwwk/DeskCraft" style="display: flex; align-items: center; gap: 8px; font-size: 16px; font-weight: 600; color: #2f80ed; text-decoration: none; margin-bottom: 10px;">
      <svg height="16" width="16" viewBox="0 0 16 16" fill="#586069" aria-hidden="true" style="flex-shrink: 0;"><path d="M2 2.5A2.5 2.5 0 0 1 4.5 0h8.75a.75.75 0 0 1 .75.75v12.5a.75.75 0 0 1-.75.75h-2.5a.75.75 0 0 1 0-1.5h1.75v-2h-8a1 1 0 0 0-.714 1.7.75.75 0 1 1-1.072 1.05A2.495 2.495 0 0 1 2 11.5Zm10.5-1h-8a1 1 0 0 0-1 1v6.708A2.486 2.486 0 0 1 4.5 9h8ZM5 12.25a.25.25 0 0 1 .25-.25h3.5a.25.25 0 0 1 .25.25v3.25a.25.25 0 0 1-.4.2l-1.45-1.087a.249.249 0 0 0-.3 0L5.4 15.7a.25.25 0 0 1-.4-.2Z"></path></svg>
      mrwwk/DeskCraft
    </a>
    <p style="font-size: 13.5px; color: #586069; line-height: 1.6; margin: 0 0 14px;">A benchmark for desktop GUI agents with 538 executable tasks in a live Ubuntu environment, covering professional workflows and human-in-the-loop collaboration.</p>
    <iframe src="https://ghbtns.com/github-btn.html?user=mrwwk&repo=DeskCraft&type=star&count=true" frameborder="0" scrolling="0" width="150" height="20" title="Star mrwwk/DeskCraft on GitHub" style="margin-top: auto;"></iframe>
  </div>
  <div style="flex: 1 1 280px; min-width: 260px; border: 1px solid #e4e2e2; border-radius: 6px; padding: 18px 20px; display: flex; flex-direction: column;">
    <a href="https://github.com/zjukg/UILoop" style="display: flex; align-items: center; gap: 8px; font-size: 16px; font-weight: 600; color: #2f80ed; text-decoration: none; margin-bottom: 10px;">
      <svg height="16" width="16" viewBox="0 0 16 16" fill="#586069" aria-hidden="true" style="flex-shrink: 0;"><path d="M2 2.5A2.5 2.5 0 0 1 4.5 0h8.75a.75.75 0 0 1 .75.75v12.5a.75.75 0 0 1-.75.75h-2.5a.75.75 0 0 1 0-1.5h1.75v-2h-8a1 1 0 0 0-.714 1.7.75.75 0 1 1-1.072 1.05A2.495 2.495 0 0 1 2 11.5Zm10.5-1h-8a1 1 0 0 0-1 1v6.708A2.486 2.486 0 0 1 4.5 9h8ZM5 12.25a.25.25 0 0 1 .25-.25h3.5a.25.25 0 0 1 .25.25v3.25a.25.25 0 0 1-.4.2l-1.45-1.087a.249.249 0 0 0-.3 0L5.4 15.7a.25.25 0 0 1-.4-.2Z"></path></svg>
      zjukg/UILoop
    </a>
    <p style="font-size: 13.5px; color: #586069; line-height: 1.6; margin: 0 0 14px;">A UI-in-the-loop paradigm for multimodal GUI reasoning, reframing the screen-to-action process as a cyclic &ldquo;Screen&ndash;UI Elements&ndash;Action&rdquo; loop for GUI agents.</p>
    <iframe src="https://ghbtns.com/github-btn.html?user=zjukg&repo=UILoop&type=star&count=true" frameborder="0" scrolling="0" width="150" height="20" title="Star zjukg/UILoop on GitHub" style="margin-top: auto;"></iframe>
  </div>
</div>


# 🎖 Honors and Awards
- *2025.06* Outstanding Graduates of Tongji University
- *2024.12* Outstanding student of Tongji University (Top 5%)
- *2024.12* Scholarship of Tongji University
- *2023.12* Scholarship of Tongji University
- *2022.12* Outstanding student of Tongji University (Top 5%)
- *2022.12* Scholarship of Tongji University

# 📖 Educations
- *2025.09 - present*, Master, Artificial Intelligence, Zhejiang University.
- *2021.09 - 2025.06*, Undergraduate, Software Engineering, Tongji University.

# 💻 Internships
- *2026.06 - present*, Alibaba Taotian Group, Meta-Code LLM Team, China.
- *2025.08 - 2026.05*, Huawei Markov Lab, China.
- *2025.03 - 2025.05*, [Huawei Noah’s Ark Lab](http://dev3.noahlab.com.hk/index.html), China.
