---
layout: home
title: Home
---

# Research Data Hub

Open access datasets for [field of research]. 

## Quick Access

- [Browse all datasets](/datasets)
- [Download guide](/guide)
- [Cite our work](/about)

## Featured Datasets

{% for dataset in site.datasets limit:3 %}
- **[{{ dataset.title }}]({{ dataset.url }})** — {{ dataset.description | truncate: 100 }}
{% endfor %}

### Quick Links
- 📧 [Contact me](mailto:pamela.vinueza@espoch.edu.ec)
- 🔬 [ResearchGate Profile](https://www.researchgate.net/profile/Marlon-Calispa)
- 📚 [View Publications](/publications/)
- 🔍 [Research Projects](/research/)
