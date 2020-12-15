# Let it snow

"Let it snow" is a lightweight, easy to modify jQuery plugin to add unobtrusive, non-blocking CSS3 snowfall to your page.

This is an updated fork with the following changes:

- Use SVG snowflakes instead of PNG for optimum quality
- Dropped support for IE9 or lower
- Removed Prefixfree, no longer needed with modern browsers
- Removed Modernizer, no longer needed with modern browsers
- Removed JS animation fallback
- Updated index.html demo, removed background image
- Updated jQuery version
- Updated Readme

## Features

- Only 0.6kb gzipped
- CSS3 animation
- Mobile support
- Disabled pointer events to prevent blocking the UI
- Attach to any container, not just the body

## Prerequisites

- Requires [jQuery](https://jquery.com/download/).

## Using

### Add prerequisites

```html
<script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
```

### Add plugin files:

```html
<link rel="stylesheet" href="css/letitsnow.css">
<script src="js/letitsnow.min.js"></script>
```

### Use on any container, eg. on the body:

```html
<script>
    $(function() {
        $('body').letItSnow();
    });
</script>
```

You can use on other container elements, for eg. a div with the id "box":

```js
$('#box').letItSnow();
```

It's advised to add **overflow-x: hidden** or **overflow: hidden** to the container element!

## Configuration

You have to dive a little into the source if you want to modify the animation.

### Slower or faster snowflakes

In the *letitsnow.css* you have to modify the rules started with **.let_it_snow.snow_duration_**. The plugin randomly choose one of these rules to create snowflake animation. You have to modify *letitsnow.js* to set the animation durations for IE (search for **.animate**)

### Shorter or longer snowflake routes

In the *letitsnow.css* you have to modify the keyframes started with **snow_anim_**. The plugin randomly choose one of these rules to create snowflake animation. You have to modify *letitsnow.js* to set the snowflake route length for IE (search for **.animate**)

## License

MIT licensed

Copyright (C) 2012 Fincza András, http://drawain.hu
