---
layout: page
permalink: /zh/repositories/
title: 图库
description: 展示团队/个人 GitHub 账号与仓库列表。
nav: true
nav_order: 4
lang: zh
ref: repositories
---

{% if site.data.repositories.github_users %}
## GitHub 用户
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>
{% endif %}

{% if site.data.repositories.github_repos %}
## GitHub 仓库
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
