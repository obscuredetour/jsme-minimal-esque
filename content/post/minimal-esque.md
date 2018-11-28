---
title: "Minimal-esque dark theme for Hugo"
date: 2018-10-07
tags: ["hugo", "web-development", "sass", "css"]
draft: false
time: "4"
image: '/images/hugo-logo-banner.png'
description: 'A quick and lightweight fully responsive dark theme for Hugo.'
---

<!-- {{< figure class="image fit" src="/images/rolling-tv-cart.jpg" >}} -->

# Minimal-esque
A dark minimal-esque blog theme for [Hugo](https://gohugo.io).

- Lightweight
- Dependency free
- Fully responsive
- Includes [Simply Navigation](https://github.com/obscuredetour/simply-nav), a dead simple lightweight navigation for all devices built with Flexbox and vanilla JS. [Demo simply navigation](https://obscuredetour.github.io/simply-nav/)

This very [blog](https://blog.jeffreysummers.me) is using this theme.

This theme was created using the [Minimal](https://github.com/calintat/minimal) blog theme as a boilerplate and was inspired by the Ghost [Casper](https://github.com/TryGhost/Casper) theme.


## Changes
Here are the most notable changes from [Minimal](https://github.com/calintat/minimal)

* Removal of Bootstrap, jQuery and all their dependencies. Yet still fully responsive.
* Article card layout built using Flexbox only.
* Bundled navigation, see [Simply Navigation](https://github.com/obscuredetour/simply-nav).


## Installation

You can install the theme either as a clone or submodule.

I recommend the latter. From the root of your Hugo site, type the following:

```
$ git submodule add https://github.com/obscuredetour/minimal-esque.git themes/minimal-esque
$ git submodule init
$ git submodule update
```

Now you can get updates to Minimal-esque in the future by updating the submodule:

```
$ git submodule update --remote themes/minimal-esque
```

## Configuration

After installation, take a look at the `exampleSite` folder inside `themes/minimal-esque`.

To get started, copy the `config.toml` file inside `exampleSite` to the root of your Hugo site:

```
$ cp themes/minimal-esque/exampleSite/config.toml .
```

Now edit this file and add your own information. Note that some fields can be omitted.

I recommend you use the theme's archetypes so now delete your site's `archetypes/default.md`.

### Post Markdown
The beginning of each post will include the following at the top of the file
```
---
title: "Post title"
date: 2018-09-23
time: "8"
image: "/images/post-image.jpg"
description: 'A description or snippet that you want displayed on the article card'
tags: ["web-development", "design", "css"]
---
```
If no image is available for the post then omit the `image:` property and replace it with the following line:  `noImage: "no-image"`. See the example below. This simply adds a `no-image` class to the HTML element.
```
---
title: "Post title"
noImage: "no-image"
...
```

### Logo
Replace the `logo-obj.svg` file within the `static` directory with one of your own.

### Customization

Options might be revisted in the future.

<!--## Features

You can tweak the look of the theme to suit your needs in a number of ways:

 - The accent colours can be changed by using the `accent` field in `config.toml`.

- You can also change the background colour by using `backgroundColor`.

For best results, I recommend you use a dark accent colour with a light background, for example:

```sass
[params]
    accent = "red"
    showBorder = true
    backgroundColor = "white"
```

### Fonts

The theme uses [Google Fonts](https://fonts.google.com) to load its font. To change the font:

```toml
[params]
    font = "Raleway" # should match the name on Google Fonts!
``` -->

### Syntax highlighting

The theme supports syntax highlighting thanks to [highlight.js](https://highlightjs.org).

It's disabled by default, so you have to enable it by setting `highlight` to `true` in your config.

You can change the style used for the highlighting by using the `highlightStyle` field.

Only the "common" languages will be loaded by default. To load more, use `highlightLanguages`.

A list of all the available styles and languages can be found [here](https://highlightjs.org/static/demo/).

Please note the style and languages should be written in hyphen-separated lowercase, for example:

```toml
[params]
    highlight = true
    highlightStyle = "solarized-dark"
    highlightLanguages = ["go", "haskell", "kotlin", "scala", "swift"]
```
