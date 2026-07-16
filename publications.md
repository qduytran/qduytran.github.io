---
layout: page
title: Publications
permalink: /publications/
---

# Overview

Research Timeline

Bachelor → Master → Research

---

# Undergraduate Thesis

Title

Supervisor

Abstract

PDF

---

# Master Thesis

Title

Supervisor

Progress

---

# Awards

{% for award in site.data.awards %}
- {{award.year}} — {{award.name}}
{% endfor %}

---

# Publications

## 2026

{% for paper in site.data.publications %}

{% if paper.year == 2026 %}

### {{paper.title}}

Authors

Journal

PDF

DOI

{% endif %}

{% endfor %}

---

## 2025

...
