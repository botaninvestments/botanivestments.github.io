---
title: Botan Investments
layout: default
---

<div class="container-full">
 {% include about.md %}
 {% include activity.md %}
 {% for post in site.posts %}
  <div class="row post">
    <div class="two columns skip"></div>
    <div class="seven columns post-title">
      <h5><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h5><br>
    </div>
  </div>
  <div class="row">
    <div class="two columns skip"></div>
    {% if post.thumbnail %}
    <div class="four columns"><img class="post-thumbnail" src="{{ post.thumbnail | prepend: site.baseurl }}" alt="{{ post.title }}" /></div>
    <div class="four columns">{{ post.excerpt }}</div>
    {% else %}
    <div class="eight columns">{{ post.excerpt }}</div>
    {% endif %}
  </div>
  {% if post.excerpt != post.content %}
  <div class="row">
    <div class="six columns skip"></div>
    <div class="four columns"><a href="{{ post.url | prepend: site.baseurl }}">Читать дальше &#8594;</a></div>
  </div>
  {% endif %}
{% endfor %}
</div>
