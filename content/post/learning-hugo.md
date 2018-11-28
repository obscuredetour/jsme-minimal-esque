---
title: "Learning Hugo"
date: 2018-10-09
tags: ["rant", "hugo", "web-development", "javascript"]
draft: false
time: "3"
# image: '/images/hugo-logo-banner.svg'
image: 'https://images.unsplash.com/photo-1532339742492-846276c31472?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=140ff93586087dc30980d1459b5401c3&dpr=1&auto=format&fit=crop&w=1000&q=80&cs=tinysrgb'
description: 'Ever start a project and get half way through it only to realize that you now have multiple projects? A story of learning Hugo, creating new Hugo themes and writing blogs.'
---

<!-- {{< figure class="image fit" src="/images/rolling-tv-cart.jpg" >}} -->

# It starts with a project

Do you ever start a project and get half way through it only to realize that you now have multiple projects? I recently found my way into this rabbit hole. Ultimately, it resulted in this post and very blog.

It all began as a way to continue my endeavor of learning more about web development. Should that count as the initial project? Well, then an idea about a rewrite on a site I built last year got me thinking. I could build it in a static site generator like [Hugo](https://gohugo.io). So, I dabbled into static site generators, and dove into Hugo. Soon after, it was all exploring, learning, and creating. Perhaps, some tinkering and tweaking too. And still am.

Then life happened. Holidays. Some people travel for said holidays and other people visit. So my initial projects (below) while doing everything else, needless to say, got put on the back burner.

1. learn about static site generators 
2. rewrite an existing site using one

## And another project

Naturally, while this project is on the back burner, I attach another project to it. A blog.

1. learn about static site generators ****
2. blog (also, write for blog - *sneaky*)
3. rewrite an existing site using one

**Themes (the lead up to the next project)**

Initially, I started out cloning a theme's [repository](https://github.com/calintat/minimal). I would advise against that notion. Follow [Hugo's quick-start](https://gohugo.io/getting-started/quick-start/) and get rolling. Add in themes via a `git` submodule. Looking back, this would have saved me some time.

## New theme (the next project)

All set up using Hugo and the [Minimal](https://themes.gohugo.io/theme/minimal/) theme relatively painlessly. I then, of course, am unhappy with many of my theme choices. jQuery dependency, just for mobile navigation? Typography reset needs work? Everything is too bright. You see where this is going, right?

My blog powered by Hugo using the Minimal theme eventually became a boilerplate for a theme I then ended up creating. 

After much fiddling and writing too much CSS, I decided to create my own  Hugo theme inspired by the [Ghost Capser](https://github.com/TryGhost/Casper) theme. 

### [Minimal-esque](/post/minimal-esque/)

[Minimal-esque](https://github.com/obscuredetour/minimal-esque) is a quick and lightweight fully responsive dark blog theme for Hugo and hosted on [GitHub](https://github.com/obscuredetour/minimal-esque). Read more about it on my [last post](/post/minimal-esque/).

Recap of project(s)

1. Learn about static site generators (Hugo)
2. Create a Hugo theme
3. Create a blog website
4. Write blog posts (like this one)
5. Rewrite an existing site using Hugo

## **Navigation component**

Within the last 6 months or so I had developed a navigation bar component I had begun to reuse throughout many of my projects. So I wanted to put it out there. See it in action.

- [Simply Nav](https://obscuredetour.github.io/simply-nav/)
- [GitHub repository](https://github.com/obscuredetour/simply-nav)

You can even notice I am lazy enough that my hamburger menu style is the same everywhere. No shame, I do not care for the hamburger menu. There I said it. Also see it on CodePen below.

<p data-height="449" data-theme-id="0" data-slug-hash="XxNWLY" data-default-tab="css,result" data-user="obscuredetour" data-pen-title="Simply Navigation" class="codepen">See the Pen <a href="https://codepen.io/obscuredetour/pen/XxNWLY/">Simply Navigation</a> by Jeffrey (<a href="https://codepen.io/obscuredetour">@obscuredetour</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

That all took way longer than I had anticipated... Needless to say, don't let a project that spawns others get you down. Slowly, but surely.