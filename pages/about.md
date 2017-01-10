---
layout: page
title: About
description: 窗外雨的个人博客
keywords: 程序,易学,政治,社会
comments: true
menu: 关于
permalink: /about/
---

十岁乃习字，十二能弈棋，
十六自学码，二八始研易。
十九上「正路」，途中一眠十八秋。
「沉舟侧畔千帆过，南国十里万木春」。

## 坚信

* 做一个内心强大的人，一个人的心态，决定了一个人的一切。

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
