---
layout: site
title: Tutorials
---

Tutorial notes will be posted slightly after class. Code will be posted after the following week

---

{% for post in site.posts %}
<div class="card mb-3">
    <div class="card-body">
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p>{{ post.excerpt }}</p>
    </div>
</div>
{% endfor %}