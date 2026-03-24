---
layout: page
title: Datasets
---

## Available Datasets

Browse and download research datasets. Files hosted on GitHub are available directly; larger files redirect to external storage.

<table class="dataset-table">
  <thead>
    <tr>
      <th>Dataset</th>
      <th>Records</th>
      <th>Size</th>
      <th>Format</th>
      <th>Updated</th>
      <th>Access</th>
    </tr>
  </thead>
  <tbody>
    {% for ds in site.data.datasets %}
    <tr>
      <td>
        <strong>{{ ds.title }}</strong><br>
        <small>{{ ds.description }}</small>
      </td>
      <td>{{ ds.records | number }}</td>
      <td>{{ ds.size }}</td>
      <td><code>{{ ds.format }}</code></td>
      <td>{{ ds.date_added }}</td>
      <td>
        {% if ds.direct_download %}
          <a href="{{ ds.url }}" class="btn btn-small" download>Download</a>
        {% else %}
          <a href="{{ ds.url }}" class="btn btn-small btn-external" target="_blank">Go to {{ ds.provider }}</a>
          {% if ds.access_instructions %}
            <br><small>{{ ds.access_instructions }}</small>
          {% endif %}
        {% endif %}
      </td>
    </tr>
    {% endfor %}
  </tbody>
</table>

## Data Usage

All datasets are released under [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) unless otherwise noted. Please cite using the DOI provided on each dataset page.

## Request New Data

Need additional variables or formats? [Open an issue](https://github.com/username/username.github.io/issues) with your request.
