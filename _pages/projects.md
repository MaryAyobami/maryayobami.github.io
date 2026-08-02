---
layout: page
title: research
permalink: /research/
description:
nav: true
nav_order: 1
---

<div class="research-statement">
  <p>
    My research centers on <strong>trustworthy, efficient computation</strong>. I am interested in security, privacy, verifiable trust, and performance, with the goal of ensuring that execution remains protected in shared environments and that results are reliable without sacrificing efficiency.
  </p>
  <p class="research-statement-close">
    I have had the opportunity to explore these questions through the following research areas.
  </p>
</div>

<div class="research-areas">

  <div class="research-area">
    <div class="research-area-label">
      <h2>Confidential Computing</h2>
    </div>
    <div class="research-area-body">
      <p>I work on enabling users to run workloads on third-party cloud infrastructure with provable confidentiality and integrity guarantees while preserving the performance that makes cloud computing viable. This involves leveraging hardware-assisted Trusted Execution Environments (TEEs) to secure data in use.</p>
      <div class="research-projects">
        {% assign cc_projects = site.projects | where: "category", "Confidential Computing" | sort: "importance" %}
        {% for project in cc_projects %}
        <div class="research-project-item">
          <a href="{{ project.url | relative_url }}" class="research-project-title">{{ project.title }}</a>
          <p class="research-project-desc">{{ project.description }}</p>
        </div>
        {% endfor %}
      </div>
    </div>
  </div>

  <div class="research-area">
    <div class="research-area-label">
      <h2>Empirical Systems Research</h2>
    </div>
    <div class="research-area-body">
      <p>I investigate performance variability in systems experiments. My goal is to help researchers trust that their measurements are representative and reproducible, rather than artifacts of environmental interference.</p>
      <div class="research-projects">
        {% assign emp_projects = site.projects | where: "category", "Empirical Systems Research" | sort: "importance" %}
        {% for project in emp_projects %}
        <div class="research-project-item">
          <a href="{{ project.url | relative_url }}" class="research-project-title">{{ project.title }}</a>
          <p class="research-project-desc">{{ project.description }}</p>
        </div>
        {% endfor %}
      </div>
    </div>
  </div>

</div>
