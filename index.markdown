---
layout: default
title: meowpricot.art!
images:
    - image_path: /assets/img/art/ishale.webp
      title: commission for ishale
    - image_path: /assets/img/art/lotus.webp
      title: commission for lotus
    - image_path: /assets/img/art/bubbles.webp
      title: commission for bubbles
updates:
    - update_date: may 28 2025
      update_content: added gallery & carousel, art page
    - update_date: may 27 2025
      update_content: layout refresh
---
<script src="https://cdn.jsdelivr.net/npm/@fancyapps/ui@5.0/dist/carousel/carousel.umd.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fancyapps/ui@5.0/dist/carousel/carousel.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fancyapps/ui@5.0/dist/carousel/carousel.thumbs.css">
<script src="https://cdn.jsdelivr.net/npm/@fancyapps/ui@5.0/dist/carousel/carousel.thumbs.umd.js"></script>

hello, i'm em!<br>
i'm a freelance illustrator from australia.

<div class="flex">

<div class="index-stuff">
<h2>updates</h2>
    <ul>
        {% for update in page.updates %}
            <li><b>{{ update.update_date }}</b>
            <br>{{ update.update_content }}</li>
            <hr>
        {% endfor %}
    </ul>
</div>

<div class="index-gallery">
<h2>gallery</h2>
    <div class="f-carousel" id="myCarousel">
    {% for image in page.images %}
        <div class="f-carousel__slide" data-thumb-src="{{ image.image_path }}">
        <a class="gallery-img" data-fancybox="gallery" data-src="{{ image.image_path }}" data-caption="{{ image.title }}"><img class="gallery-img" src="{{ image.image_path }}" alt="{{ image.title }}"/></a>
        </div>
    {% endfor %}
    </div>
</div>

</div>

<script>
    new Carousel(document.getElementById("myCarousel"), {
        // Your custom options
        Dots: false,
        Thumbs: {
          type: "classic",
        },
      }, { Thumbs });
    Fancybox.bind('[data-fancybox]', {
        // Your custom options
      });
</script>