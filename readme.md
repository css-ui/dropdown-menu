## Dropdown menu

Simple dropdown menu.

## Installation

```
npm install --save css-ui-dropdown-menu
```

## Demo

- https://css-ui.github.io/dropdown.menu

## Quick start

CSS dependencies.

```html
<link rel="stylesheet" href="path/to/normalize.css">
<link rel="stylesheet" href="path/to/font-awesome.css">
<link rel="stylesheet" href="path/to/open-sans.css">
<link rel="stylesheet" href="path/to/cssui.css">
```

CSS dropdown style.

```html
<link rel="stylesheet" href="path/to/style.dropdown.css">
```

CSS light or dark theme for menu. Choose one.

```html
<link rel="stylesheet" href="path/to/style.dropdown.light.css">
<link rel="stylesheet" href="path/to/style.dropdown.dark.css">
```

Set font.

```html
<style>
	body {
		font-family: 'Open Sans', sans-serif;
	}
</style>
```

Dropdown menu html.

```html
<div class="dropdown">

	<!-- dropdown menu click -->
	<div class="clear">
		<a class="employ-toggle click float right" href="#">
			<i class="fa fa-ellipsis-v" aria-hidden="true"></i>
		</a>
	</div>

	<!-- show/hide menu -->
	<ul class="expand-dropdown">
		<li><a href="#" class="top">One</a></li>
		<li><a href="#">Two</a></li>
		<li><a href="#" class="bottom">Three</a></li>
	</ul>
</div>
```

javascript libraries and plugins.

```html
<script src="path/to/jquery.js"></script>
<script>
	$(function() {
		$('.employ-toggle').on('click', function() {
			var dropdown = '.expand-dropdown';
			$(dropdown).fadeToggle('fast');
			$(dropdown).on('click', function(e) {
				var target = e.target;
				var employ = '.employ-toggle';
				if (!$(target).is(employ) && !$(target).parents().is(employ)) {
					$(dropdown).hide();
				}
			});
		});
	});
</script>
```
