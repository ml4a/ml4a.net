---
layout: default
title: Machine learning for arts
---

<!--

  About
  Artworks
  Support / contribute (sponsors, cryptoart)


-->





<div class="collapse bg-dark" id="navbarHeader">
  <div class="container">
    <div class="row">
      <div class="col-sm-8 col-md-7 py-4">
        <h4 class="text-white">About</h4>
        <p class="text-muted">Add some information about the album below, the author, or any other background context. Make it a few sentences long so folks can pick up some informative tidbits. Then, link them off to some social networking sites or contact information.</p>
      </div>
      <div class="col-sm-4 offset-md-1 py-4">
        <h4 class="text-white">Contact</h4>
        <ul class="list-unstyled">
          <li><a href="#" class="text-white">Follow on Twitter</a></li>
          <li><a href="#" class="text-white">Like on Facebook</a></li>
          <li><a href="#" class="text-white">Email me</a></li>
        </ul>
      </div>
    </div>
  </div>
</div>



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
        <a href="#" class="btn btn-primary my-2">Tag 1</a>
        <a href="#" class="btn btn-secondary my-2">Tag 2</a>
        <a href="#" class="btn btn-secondary my-2">Tag 3</a>
        <a href="#" class="btn btn-secondary my-2">Tag 4</a>
        <a href="#" class="btn btn-secondary my-2">Tag 5</a>
      </p>
    </div>
  </section>

  <div class="album py-5 bg-light">
    <div class="container-xl">
      <div class="row">
        {% for guide in site.data.guides %}
          
          {% assign name = guide[0] %}
          {% assign title = guide[1].title %}
          {% assign description = guide[1].description %}
          {% assign colab = guide[1].colab %}
          {% assign thumb = guide[1].thumb %}
          {% assign category = guide[1].category %}
          {% assign summary = guide[1].summary %}
      
          <div class="col-md-4">
            <div class="card mb-4 shadow-sm">
              <img class="img-thumbnail" src="{{thumb}}" alt="{{title}}">
              <div class="card-body">
                <h5 class="card-title">{{title}}</h5>
                <p class="card-text">{{description}}</p>
                <a href="{{colab}}" class="btn btn-outline-primary"><img src="/images/icons/github.png">&nbsp;&nbsp;View code</a>
                <a href="{{colab}}" class="btn btn-outline-primary"><img src="/images/icons/colab.png">&nbsp;&nbsp;Open in Colab</a>
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

