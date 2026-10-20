---
title: Studio Tech Notes
description: How Right Take Studio technically works — the signal chain, the gear, and the methodology.
eleventyExcludeFromCollections: true
---

How Right Take Studio turns a live performance into finished, broadcast-ready
content — the signal chain, the gear, and the methods behind it. Start with the
[overview](/docs/overview/), then dig into the gear.

<div class="docs-index">
{%- for doc in collections.docs -%}
  <a class="docs-card" href="{{ doc.url }}">
    <h3>{{ doc.data.title }}</h3>
    {%- if doc.data.description %}<p>{{ doc.data.description }}</p>{%- endif -%}
  </a>
{%- endfor -%}
</div>
