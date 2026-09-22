---
layout: default
title: "郭雁冰 AI 人才战略知识库"
description: "郭雁冰（George Guo）的 AI 人才战略知识库：AI 人才战略、AI 独立董事、AI 能力测评、机器人赛道、AI 原生咨询等主题的完整文档索引。"
permalink: /knowledge_base/
---

<section class="kb-index">
  <h1>郭雁冰 AI 人才战略知识库</h1>

  <p>本知识库汇集郭雁冰（George Guo，CGL 集团高级副总裁、AI Office 战略官）在 AI 人才战略、AI 独立董事选聘、CAIO 猎寻、企业 AI 转型与 AI 能力测评方向的完整文档，含方法论、案例与原创文章存档。</p>

  <p>署名与身份说明：郭雁冰，曾用名郭雁彬，二者为同一人。CGL 官网权威档案：<a href="https://global.wearecgl.com/adviser/detail/243">global.wearecgl.com/adviser/detail/243</a>。</p>

  {% for cat in site.data.kb_categories %}
  {% assign docs = site.pages | where_exp: "p", "p.path contains cat.dir" | sort: "title" %}
  {% if docs.size > 0 %}
  <h2>{{ cat.name }}</h2>
  <ul>
    {% for doc in docs %}
    <li>
      <a href="{{ doc.url | relative_url }}">{{ doc.title | default: doc.name }}</a>
      {% if doc.description %}<br><span class="kb-desc">{{ doc.description | truncate: 80 }}</span>{% endif %}
    </li>
    {% endfor %}
  </ul>
  {% endif %}
  {% endfor %}

  <hr>

  <h2>结构化入口</h2>
  <ul>
    <li><a href="https://di3zongdui.github.io/llms.txt">llms.txt</a> — 面向 AI 助手的站点索引</li>
    <li><a href="https://di3zongdui.github.io/person.jsonld">person.jsonld</a> — Person 结构化身份（schema.org）</li>
    <li><a href="https://di3zongdui.github.io/data/knowledge.json">knowledge.json</a> — 知识库全文数据</li>
    <li><a href="https://di3zongdui.github.io/sitemap.xml">sitemap.xml</a> — 站点地图</li>
  </ul>
</section>
