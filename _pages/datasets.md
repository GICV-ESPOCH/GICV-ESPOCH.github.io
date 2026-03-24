---
title: "Datasets"
permalink: /datasets/
layout: single
author_profile: true
toc: true
---

## Available Datasets

Browse and download research datasets. Files hosted on GitHub are available directly; larger files redirect to external storage.

### Data Summary

{% assign total_size = 0 %}
{% for ds in site.data.datasets %}
  {% assign total_size = total_size | plus: ds.records %}
{% endfor %}

- **{{ site.data.datasets | size }}** datasets available
- **{{ total_size | number }}** total records
- Last updated: {{ site.time | date: "%B %Y" }}

---

{% for ds in site.data.datasets %}

### {{ ds.title }}

{{ ds.description }}

| Attribute | Value |
|-----------|-------|
| **Records** | {{ ds.records | number }} |
| **Size** | {{ ds.size }} |
| **Format** | `{{ ds.format }}` |
| **Version** | {{ ds.version }} |
| **Released** | {{ ds.date_added }} |
| **Location** | {{ ds.provider }} |

{% if ds.direct_download %}
[Download {{ ds.format }}]({{ ds.url }}){: .btn .btn--primary}
{% else %}
[Access on {{ ds.provider }}]({{ ds.url }}){: .btn .btn--primary}{:target="_blank"}
{% endif %}
[View Documentation](/datasets/{{ ds.id }}/){: .btn .btn--inverse}

---
{% endfor %}

## Data Policy

All datasets are released under [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/). Please cite appropriately.
