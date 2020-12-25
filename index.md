---
layout: default
title: Machine learning for arts
---

<!--

  About
  Artworks
  Support / contribute (sponsors, cryptoart)
  Classes
  Book
  Demos

-->







<nav class="navbar navbar-expand-md navbar-dark bg-dark">
  <a class="navbar-brand" href="#">Expand at md</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarsExample04" aria-controls="navbarsExample04" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarsExample04">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item active">
        <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Link</a>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
      </li>
      <li class="nav-item dropdown">
        <a class="nav-link dropdown-toggle" href="#" id="dropdown04" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">Dropdown</a>
        <div class="dropdown-menu" aria-labelledby="dropdown04">
          <a class="dropdown-item" href="#">Action</a>
          <a class="dropdown-item" href="#">Another action</a>
          <a class="dropdown-item" href="#">Something else here</a>
        </div>
      </li>
    </ul>
    <form class="form-inline my-2 my-md-0">
      <input class="form-control" type="text" placeholder="Search">
    </form>
  </div>
</nav>





<main role="main">

  <section class="jumbotron text-center">
    <div class="container">
      <h1>Machine Learning for Art</h1>
      <p class="lead text-muted">ml4a is a collection of tools and educational resources which apply techniques from machine learning to arts and creativity.</p>
      <p>
        <a href="#" class="btn btn-primary my-2">Models</a>
        <a href="#" class="btn btn-secondary my-2">Fundamentals</a>
        <a href="#" class="btn btn-secondary my-2">ml5.js</a>
      </p>
    </div>
  </section>



  <div class="album py-5 bg-light">
    <div class="container-xl">
      <div class="row">
        {% for guide in site.data.guides2 %}
          
          {% assign name = guide[0] %}
          {% assign title = guide[1].title %}
          {% assign description = guide[1].description %}
          {% assign github = guide[1].github %}

          <div class="col-md-4">
            <div class="card mb-4 shadow-sm">
              
              {% if guide[1].video_thumb %}
              <video loop autoplay >
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
                <a href="https://github.com/ml4a/ml4a/blob/ml4a.net/{{github}}" class="btn btn-outline-primary"><img src="/images/icons/github.png">&nbsp;&nbsp;View code</a>
                <a href="https://colab.research.google.com/github/ml4a/ml4a-guides/blob/ml4a.net/{{github}}" class="btn btn-outline-primary"><img src="/images/icons/colab.png">&nbsp;&nbsp;Open in Colab</a>
              </div>
            </div>
          </div>
    
        {% endfor %}
        
      </div>
    </div>
  </div>

</main>


<footer class="text-muted">
  <div class="container">
    <p class="float-right">
      <a href="#">Back to top</a>
    </p>
    <p>Album example is &copy; Bootstrap, but please download and customize it for yourself!</p>
    <p>New to Bootstrap? <a href="https://getbootstrap.com/">Visit the homepage</a> or read our <a href="../getting-started/introduction/">getting started guide</a>.</p>
  </div>
</footer>

