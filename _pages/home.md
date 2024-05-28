---
layout: splash
permalink: /
hidden: true
header:
  overlay_color: "#000000"

excerpt: >
  Crea, comparte, aprende y disfruta.<br />
  <small><a href="https://github.com/trastejant"><i class="fab fa-github"></i></a></small> 
  ·
  <small><a href="https://twitter.com/trastejant"><i class="fab fa-fw fa-twitter-square"></i></a></small> 
  ·
  <small><a href="https://youtube.com/trastejant"><i class="fab fa-youtube"></i></a></small> 
feature_row:
  - image_path: /assets/images/bloque-proyectos.png
    alt: "customizable"
    title: "Proyectos"
    excerpt: "Proyectos documentados y explicados paso a paso para que puedas desarrollarlos."
    url: "/proyectos/"
    btn_class: "btn--primary"
    btn_label: "Ver más"
  - image_path: /assets/images/bloque-eventos.png
    alt: "fully responsive"
    title: "Blog"
    excerpt: "Noticias sobre el mundo del Hardware Libre, eventos y competiciones."
    url: "/year-archive/"
    btn_class: "btn--primary"
    btn_label: "Ver más"
  - image_path: /assets/images/bloque-tutoriales.png
    alt: "100% free"
    title: "Tutoriales"
    excerpt: "Tutoriales sobre electronica y el uso de los sensores y actuadores más comunes."
    url: "/tutoriales/"
    btn_class: "btn--primary"
    btn_label: "Ver más"      
---

{% include feature_row %}

## ¿Que es el Hardware Libre?

Se llama hardware libre, hardware de código abierto, electrónica libre o máquinas libres a aquellos dispositivos de hardware cuyas especificaciones y diagramas esquemáticos son de acceso público, ya sea bajo algún tipo de pago, o de forma gratuita.

Dicho de otra forma, decimos que un proyecto es abierto cuando podemos encontrar toda la documentación necesaria para saber como está hecho y como funciona, de forma que podamos aprender, crearlo nosotros mismos, o mejorar el diseño original y hacer que siga creciendo.

El Hardware Libre, al igual que su homologo en el mundo del software permite compartir el conocimiento, crear cultura y hacerla accesible a todos. De esta forma fomentamos que más gente pueda aprender de nuestros aciertos y nuestros errores, aportamos nuevas ideas y fomentamos el desarrollo y la investigación, no solo de la tecnología, sino de cualquier ciencia y ambiente.

## Ultimas entradas:

<div class = "last_post">
{% for post in site.posts limit:4 %}
<div class = "grid__item">

  <article class = "archive__item">
    <div class = "archive__item-teaser">
      <img src="{{post.header.image}}" alt="">
    </div>
    <h2><a href="{{post.url}}">{{post.title}}</a></h2>
      <p class="page__meta">
      <span class="page__meta-readtime">
        <i class="far fa-clock" aria-hidden="true"></i>
          {{ post.date | date_to_string  }}
      </span>
      </p>
    <p class="archive__item-excerpt" itemprop="description">{{post.excerpt | strip_html | truncatewords: 30}}</p>
  </article>
</div>
{% endfor %}

</div>

<a href="#page-title" class="back-to-top">{{ site.data.ui-text[site.locale].back_to_top | default: 'Back to Top' }} &uarr;</a>
