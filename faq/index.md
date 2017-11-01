---
title: FAQ
overview: Frequently Asked Questions about Istio.
layout: faq
type: markdown
---
{% include home.html %}

# Layihə ilə bağlı bəzi detallar

Yeni sual, fikir, təklif, iradlar üçün: [GOUPAZ Forum](https://groups.google.com/forum/#!forum/goupaz) 

{% assign faqs = site.faq | sort: "order" %}
<div class="panel-group" id="accordion">

  {% for q in faqs %}
	  {% assign name = q.path | downcase | split: '/' | last | remove: ".md" %}

  <div id="{{name}}" class="panel panel-default">
    <div class="panel-heading">
      <h4 class="panel-title">
        <a data-toggle="collapse" data-parent="#accordion" href="#collapse{{forloop.index}}">
          {{q.title}}
        </a>
      </h4>
    </div>

    <div id="collapse{{forloop.index}}" class="panel-collapse collapse">
      <div class="panel-body">
        {{q.content}}
      </div>
    </div>
  </div>
  {% endfor %}
</div>
