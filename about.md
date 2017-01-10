---
layout: default
title: About
permalink: /about/
---

<div class="about">
  <div class="container">
    <div class="row">
      <div class="col-xs-12 col-lg-6">
        <div class="left" id="selected" style="background-image: url('{{ site.gifs.last.gif_url }}');">
          <!-- This contains the animation -->
        </div>
      </div>
      <div class="col-xs-12 col-lg-6">
        <div class="right">
          <h3>
            We love <span>giphy's</span>.
          </h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quidem excepturi saepe aspernatur cupiditate, autem dolore quas voluptas architecto tempora, praesentium ex velit deserunt ea delectus porro. Rem porro repudiandae voluptatum, mollitia ex voluptas, accusantium saepe perspiciatis laboriosam, perferendis alias quae!
          </p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptas, aut asperiores porro tempore recusandae dignissimos adipisci ex, optio, quo aliquam cupiditate velit voluptatum. Illum, placeat.
          </p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corporis, eligendi.
          </p>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="container">
  <div class="row">
    <div class="col-xs-12 col-lg-6">
      <div class="row">
        {% for gif in site.gifs %}
        <div class="col-xs-6 col-lg-3">
          <div class="gif-item" style="background-image: url('{{ gif.gif_url }}');" data-target="{{ gif.gif_url }}">
          <div class="filter active"></div>
          </div>
        </div>
        {% endfor %}
      </div>
    </div>
    <div class="col-xs-12 col-lg-6">
    </div>
  </div>
</div>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
<script>
  $(document).ready(function() {
    $( ".gif-item" ).click(function() {
      console.log("this works")
      var target = $(this).data('target');
      var css_target = "url(" + target + ")"
      $('#selected').css("background-image",css_target )
      $('.gif-item').css('filter', 'grayscale(100%)');
      $(this).css('filter', 'none');
    });
  });
</script>



