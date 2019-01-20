---
layout: site
title: Code
---

Demo code shown in tutorial. Will be posted slightly after class. Not every tutorial will have demo code

---

### Solutions

<ul>
{% for soln in site.static_files %}
    {% if soln.path contains 'code' %}
        <li><a href="{{ site.baseurl }}{{ soln.path }}">{{ soln.name }}</a></li>
    {% endif %}
{% endfor %}
</ul>
