---
layout: page
title: About
description: 余生多学，惜无一通达。十六习码，二八学易，喜书法，尤爱中国象棋。
keywords: 程序,易学,政治,社会
comments: true
menu: 关于
permalink: /about/
---

非风动，非幡动，仁者心动。

## 坚信

* 熟能生巧
* 努力改变人生

## 联系

* GitHub：[@songmj](https://github.com/songhaoxin)
* 博客：[{{ site.title }}]({{ site.url }})

## Skill Keywords

#### Software Engineer Keywords
<div class="btn-inline">
    {% for keyword in site.skill_software_keywords %}
    <button class="btn btn-outline" type="button">{{ keyword }}</button>
    {% endfor %}
</div>

#### Mobile Developer Keywords
<div class="btn-inline">
    {% for keyword in site.skill_mobile_app_keywords %}
    <button class="btn btn-outline" type="button">{{ keyword }}</button>
    {% endfor %}
</div>

#### Windows Developer Keywords
<div class="btn-inline">
    {% for keyword in site.skill_windows_keywords %}
    <button class="btn btn-outline" type="button">{{ keyword }}</button>
    {% endfor %}
</div>

#### 易学技能
<div class="btn-inline">
    {% for keyword in site.skill_yii_keywords %}
    <button class="btn btn-outline" type="button">{{ keyword }}</button>
    {% endfor %}
</div>
