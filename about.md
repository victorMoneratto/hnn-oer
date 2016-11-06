---
title: Sobre
layout: page
single_page: true
---
Este site é parte do trabalho final da matéria de [Arquitetura de Computadores](https://uspdigital.usp.br/jupiterweb/obterDisciplina?sgldis=ssc0114&nomdis=) ministrada pela professora [Kalinka Regina Lucas Jaquie Castelo Branco](http://conteudo.icmc.usp.br/pessoas/kalinka/) no segundo semestre de 2016.

Desenvolvido por:

{% assign authors = site.data.authors | sort:"name" %}
{% for author in authors %}
*  {% include icon-github.html username=author.github name=author.name%}
{% endfor %}

As referências utilizadas estão no fim de cada página.