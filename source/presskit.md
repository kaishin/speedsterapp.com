---
layout: default
---

***

{% assign presskit = site.data.presskit %}

# Presskit

{{ presskit.name }}: {{ presskit.description }}

### Features

<ul>
  {% for feature in presskit.features %}
    <li>{{ feature }}</li>
  {% endfor %}
</ul>

### Roadmap

<ul>
  {% for feature in presskit.roadmap %}
    <li>{{ feature }}</li>
  {% endfor %}
</ul>

### Contact

- [Website]({{ presskit.website }})
- [Twitter](https://twitter.com/{{ presskit.twitter }})
- [Email](mailto:{{ presskit.email }})

### Assets

<a href="{{ presskit.assets_url }}" class="button">Download Assets</a>
