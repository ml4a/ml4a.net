<!doctype html>
<html lang="en">
	<head>

		{% assign title = site.title %}
		{% if page.title %} 
			{% assign title = page.title %}
		{% endif %}

		{% assign description = site.default_description %}
		{% if page.description %} 
			{% assign description = page.description %}
		{% endif %}
		
		{% assign thumbnail = site.default_thumbnail %}
		{% if page.thumbnail %} 
			{% assign thumbnail = page.thumbnail %}
		{% endif %}

		<!-- Meta -->	
		<title>{{page.title}}</title>
		<meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
		<meta name="author" content="{{site.author}}">
		<meta name="generator" content="Jekyll v4.1.1">
		<meta name="description" content="{{description}}">
		<meta name="twitter:card" content="summary" />
		<meta name="twitter:title" content="{{title}}" />
		<meta name="twitter:description" content="{{description}}" />
		<meta name="twitter:image" content="https://mars.college/{{thumbnail}}" />
		<meta property="og:title" content="{{title}}">
		<meta property="og:description" content="{{description}}" />
		<meta property="og:image" content="https://mars.college/{{thumbnail}}" />

		<!-- Favicons -->
		<link rel="apple-touch-icon" sizes="180x180" href="/images/favicon/apple-touch-icon.png">
		<link rel="icon" type="image/png" sizes="32x32" href="/images/favicon/favicon-32x32.png">
		<link rel="icon" type="image/png" sizes="16x16" href="/images/favicon/favicon-16x16.png">
		<link rel="manifest" href="/images/favicon/site.webmanifest">
		<link rel="mask-icon" href="/images/favicon/safari-pinned-tab.svg" color="#5bbad5">
		<link rel="shortcut icon" href="/images/favicon/favicon.ico">
		<meta name="msapplication-TileColor" content="#da532c">
		<meta name="msapplication-config" content="/images/favicon/browserconfig.xml">
		<meta name="theme-color" content="#ffffff">
		
		<!-- Bootstrap -->		
		<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
		<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
		<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ho+j7jyWK8fNQe+A12Hb8AhRq26LrZ/JpcUGGOn+Y7RsweNrtN/tE3MoK7ZeZDyx" crossorigin="anonymous"></script>

		<!-- Additional styling/js -->
		<link rel="stylesheet" type="text/css" href="/css/style.css">

	</head>
	
	<body>
		
		{{content}}

  </body>
	
</html>
