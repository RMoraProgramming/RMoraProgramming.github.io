---
layout: archive
perlink: /programmmingexperience/
<<<<<<< HEAD
title: "Programming Experience by tags"
=======
title: "Programming Experience"
>>>>>>> 7bdee819fb48993db6dd27df27c083aab1726098
author_profile: true
header:
image: "/images/image1.jpg"
---


{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
