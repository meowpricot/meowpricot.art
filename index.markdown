---
layout: default
title: meowpricot.art!
images:
    - image_path: /assets/img/art/ishale.webp
      title: ishale
    - image_path: /assets/img/art/lotus.webp
      title: lotus
    - image_path: /assets/img/art/hdollvt.webp
      title: hdollvt
---
hello, i'm em!<br>
i'm a freelance illustrator from australia.

<div class="fotorama" data-height="400" data-fit="cover" data-autoplay="true" data-allowfullscreen="true" data-nav="false">
  {% for image in page.images %}
    <img src="{{ image.image_path }}" alt="{{ image.title }}"/>
  {% endfor %}
</div>