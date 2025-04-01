---
title: Aula 09 - Fundamentos de VueJs
nav_order: 9
has_children: false
has_toc: false
youtubeId: 
next: ../10
---


{% assign title = page.title | split: "-"  %}
{% assign slide =  title[1] | replace: " ", "-" | prepend: page.nav_order %}

{% if page.nav_order < 10 %}
{% assign slide =   slide | prepend: "0" %}
{% endif %}


## {{ title | slice: 1 }}

### Recurso

<span class="fs-3">
  <a href="{{site.baseurl}}/assets/downloads/{{ slide }}.pdf" class="btn" target="_blank">Notas de aula</a>
<!--  <a href="https://www.icloud.com/keynote/0vGSUyeYDqiIPQYHqHpQubOAA#09-Fundamentos-de-NodeJS" class="btn" target="_blank">Notas de aula com animações</a> -->
</span>


<span class="fs-3 float-right">
[Próxima aulas]({{page.next}}){: .btn }
</span>

