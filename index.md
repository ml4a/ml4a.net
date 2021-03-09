---
layout: default
title: Machine learning for arts
---

{% include navbar.md %}

<main role="main">

  <section class="jumbotron text-center">
    <div class="container">
      <h1>Machine Learning for Art</h1>
      <p class="lead text-muted">ml4a is a collection of tools and educational resources which apply techniques from machine learning to arts and creativity.</p>
      <p>
        <a href="#" class="btn btn-primary my-2">Models</a>
        <a href="/fundamentals" class="btn btn-secondary my-2">Fundamentals</a>
        <a href="/ml5" class="btn btn-secondary my-2">ml5.js</a>
      </p>
    </div>
  </section>

  <div class="album py-5 bg-light">
    <div class="container-xl">
      <div class="row">
        {% for guide in site.data.guides.models %}
          
          {% assign name = guide[0] %}
          {% assign title = guide[1].title %}
          {% assign description = guide[1].description %}
          {% assign github = guide[1].github %}

          <div class="col-md-4">
            <div class="card mb-4 shadow-sm">
              
              {% if guide[1].video_thumb %}
              <video style="width:100%" loop autoplay >
                <source src="/images/guides/{{name}}.mp4" alt="{{title}}" type="video/mp4">
                <source src="/images/guides/{{name}}.webm" type="video/webm">
                <img src="/images/guides/{{name}}.jpg">
                </video>
              {% else %}
                <img class="img-thumbnail" src="/images/guides/{{name}}.jpg" alt="{{title}}">
              {% endif %}
                
              <div class="card-body">
                <h5 class="card-title">{{title}}</h5>
                <p class="card-text">{{description}}</p>
                <a href="https://github.com/ml4a/ml4a/blob/master/{{github}}" class="btn btn-outline-primary"><img src="/images/icons/github.png">&nbsp;&nbsp;View code</a>
                <a href="https://colab.research.google.com/github/ml4a/ml4a/blob/master/{{github}}" class="btn btn-outline-primary"><img src="/images/icons/colab.png">&nbsp;&nbsp;Open in Colab</a>
              </div>
            </div>
          </div>
    
        {% endfor %}
        
      </div>
    </div>
  </div>

</main>

{% include footer.md %}
