---
layout: post
title: 添加archive
---
创建archive.html  


```
{% raw %}
---
layout: default
title: Archive
---

<h2>Archives</h2>
<ul>
  {% for post in site.posts %}

    {% unless post.next %}
      <h3>{{ post.date | date: '%Y' }}</h3>
    {% else %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
      {% if year != nyear %}
        <h3>{{ post.date | date: '%Y' }}</h3>
      {% endif %}
    {% endunless %}

    <li>{{ post.date | date:"%b %d" }} <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
{% endraw %}
```  


