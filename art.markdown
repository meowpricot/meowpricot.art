---
layout: default
title: art!
permalink: /art/
images:
    - image_path: /assets/img/art/ishale.webp
      title: ishale
    - image_path: /assets/img/art/lotus.webp
      title: lotus
    - image_path: /assets/img/art/wazumi.webp
      title: wazumi
    - image_path: /assets/img/art/mayu.webp
      title: mayu
    - image_path: /assets/img/art/hdollvt.webp
      title: hdollvt
    - image_path: /assets/img/art/bubbles.webp
      title: bubbles
    - image_path: /assets/img/art/boomba.webp
      title: boomba
---
click for larger preview!
<script>
    Fancybox.bind('[data-fancybox]', {
        // Your custom options
      });
</script>
<div class="gallery">
  {% for image in page.images %}
    <a class="gallery-img" data-fancybox="gallery" data-src="{{ image.image_path }}" data-caption="{{ image.title }}"><img class="gallery-img" src="{{ image.image_path }}" alt="{{ image.title }}"/></a>
  {% endfor %}
</div>