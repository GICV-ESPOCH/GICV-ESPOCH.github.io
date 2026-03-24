---
title: "Datasets"
permalink: /datasets/
layout: single
author_profile: true
---

Browse and download research datasets.

| Dataset | Description | Size | Format | Access |
|---------|-------------|------|--------|--------|
{% for ds in site.data.datasets %}| **{{ ds.title }}** | {{ ds.description }} | {{ ds.size }} | {{ ds.format }} | {% if ds.direct_download %}[Download]({{ ds.url }}){: .btn .btn--small}{% else %}[{{ ds.provider }}]({{ ds.url }}){: .btn .btn--small}{% endif %} |
{% endfor %}

## Data Usage

All datasets released under CC-BY 4.0. [Citation guide](/guide/)
