---
---
<html lang="en">
	<head>
		<meta charset="utf-8">
		<meta http-equiv="X-UA-Compatible" content="IE=edge">
		<meta name="viewport" content="width=device-width, initial-scale=1">
		<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-alpha.6/css/bootstrap.min.css" integrity="sha384-rwoIResjU2yc3z8GV/NPeZWAv56rSmLldC3R/AZzGRnGxQQKnKkoFVhFQhNUwEyJ" crossorigin="anonymous">
		<script src="https://code.jquery.com/jquery-3.1.1.slim.min.js" integrity="sha384-A7FZj7v+d/sdmMqp/nOQwliLvUsJfDHW+k9Omg/a/EheAdgtzNs3hpfag6Ed950n" crossorigin="anonymous"></script>
		<script src="https://cdnjs.cloudflare.com/ajax/libs/tether/1.4.0/js/tether.min.js" integrity="sha384-DztdAPBWPRXSA/3eYEEUWrWCy7G5KFbe8fFjk5JAIxUYHKkDx6Qin1DkWx51bBrb" crossorigin="anonymous"></script>
		<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-alpha.6/js/bootstrap.min.js" integrity="sha384-vBWWzlZJ8ea9aCX4pEW3rVHjgjt7zpkNpZk+02D9phzyeVkE+jo0ieGizqPLForn" crossorigin="anonymous"></script>
		<style>
		.navbar {
			background-color: white;
			box-shadow: 0px 1px 3px -1px rgba(0,0,0,0.15);
		}
		.jumbotron {
			height: 325px;
			vertical-align: middle;
			background-image: url(http://www.ugasmis.com/uploads/8/1/3/6/81367886/background-images/363152973.jpg);
			background-repeat: no-repeat;
			background-position: 0.00% 31.48%;
			background-color: transparent;
			background-size: cover;
		}
		.jumbotron:after {
			content: '';
			position: absolute;
			top: 0;
			left: 0;
			display: block;
			width: 100%;
			min-height: 100%;
			height: inherit;
			background: rgba(0,0,0,0.35);
		}
		.jumbotron-text {
			color: white;
			z-index: 10000;
		}
		.no-lr-padding {
			padding-left: 0px;
			padding-right: 0px;
		}
		</style>
	</head>
	<body>
		<div class="container" id="header">
			<nav class="navbar navbar-toggleable-md navbar-light bg-faded">
				<button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarText" aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
				<span class="navbar-toggler-icon"></span>
				</button>
				<a class="navbar-brand" href="#">
					<img src="http://www.ugasmis.com/uploads/8/1/3/6/81367886/screen-shot-2016-09-09-at-8-57-13-pm.png" width="300" height="50" class="d-inline-block align-top" alt="">
				</a>
				<div class="collapse navbar-collapse" id="navbarText">
					<ul class="navbar-nav mr-auto">
						{% assign pages = site.pages | sort:"index" %}
						{% for my_page in pages %}
							{% if my_page.navigation_title %}
								<li class="nav-item {% if my_page.url == page.url %}active{% endif %}">
								<a class="nav-link" href="{{ my_page.url | prepend: site.baseurl }}">
									{{ my_page.navigation_title }}
								</a>
							</li>
						{% endif %}
						{% endfor %}
					</ul>
				</div>
			</nav>
		</div>
		<div class="container-fluid text-center no-lr-padding">
			<div class="jumbotron">
				<span class="jumbotron-text">
					<h3>
					The University of Georgia
					</h3>
					<h2>
					Society of Business Intelligence
					</h2>
				</span>
			</div>
		</div>
	</body>
</html>