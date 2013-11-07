---
layout: default
title: "Dart Code Samples"
header:
  css: ["/samples/samples.css"]
has_permalinks: true
---
{% injectdata samples samples/samples.yaml %}

<div class="row-fluid" markdown="1">
<div class="span3" id="toc-side" markdown="1">
{% include guide_toc.html %}
</div>

<div class="span9 offset3" markdown="1">

  <h1> {{ page.title }} </h1>

  <div class="row-fluid">
      {% for group in page.samples.col1 %}
        <h2 class="group-heading">{{ group.heading }}</h2>
        <div class="row-fluid">
          <div class="span9">
            {% for example in group.examples %}
              <div class="row-fluid example">
                <div class="span6">
                  <div class="title"><a href="{{ example.explanation_url }}">{{ example.title }}</a></div>
                </div>
                <div class="span3">
                  <div class="link"><a href="{{ example.source_url }}">Source</a></div>
                </div>
                <div class="span3">
                  {% if example.tryit_url %}
                    <a href="{{ example.tryit_url }}">Try it</a>
                  {% endif %}
                </div>
              </div>
            {% endfor %}
          </div>
          <div class="span3">
            <img class="screenshot" src="imgs/{{group.screenshot}}" >
          </div>
        </div>
      {% endfor %}

</div>
</div>
