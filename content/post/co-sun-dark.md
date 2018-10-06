---
title: Colorado Sun dark theme
date: "2018-09-23"
time: "4"
image: "/images/co-sun-bkg.jpg"
description: 'The Colorado Sun is great and brilliantly designed, but after too much reading the white background can be glaring.'
tags: [web-development, design, css]
---

# Dark theme for coloradosun.com

I really like [The Colorado Sun](https://coloradosun.com/), but after a while the white background is too much.  Their website design is fantastic, so I don't want to change too much.

The goal is to keep the same minimalistic theme with a touch of color, just darker and easier on the eyes. I am sharing it and the process of creation in hopes that it will help someone else.

So let's get after it! First is color selection and comparison. I use a tool throughout called [Contrast Ratio](https://contrast-ratio.com/) made by the brilliant [Lea Verou](http://lea.verou.me/). It always helps me balance contrast and text for maximum legibility on projects.

Skip to [screenshots](#screenshots).

## Website colors
**Background**

Colorado Sun's background is pure white `#fff`. Since their navigation bar and footer are already black I decided on charcoal `#202326`, for lack of a better name.

**Article headers**

Article headings are almost black `rgba(0,0,0,.85)`. Let's go with almost white `rgba(255,255,255,.85)`, because my goal is to change only a little and keep to their design and theme.

**Main text**

All main article text is pure black `#000` and I want mostly white `#f5f4f5` because the contrast will be plenty high enough with the new dark background color without going full blown pure white.

**Tertiary text**

The tertiary text includes all text on the secondary articles usually. Again with contrast and maximum legibility in mind and only changing what needs to be changed.

The two light greys `#8b8581`, `#7d7373` I swapped out for `#c9c9c9`,`#bcb8b6` respectively and the dark grey `#5a5653` to `#aeaeae`.

**Link text**

The links in the articles are bright blue `#2b56ff` with a bright green `#30e8bd` underline. After some fiddling around I decided to just reverse the colors to optimize contrast and keep the same vibe going.

Article bio and Credibility learn more links are blue too, but thought green looked out of place here. So I decided on CO Sun yellow `#fcd232` here.

**Buttons / Borders**

The buttons around the website are typically all CO Sun yellow `#fcd232` or the bright blue `#2b56ff`. Page and card borders are grey `#c4c2c0`. These I kept all the same except for one button.

Because the new awesome dark background is in place the all blue 'more stories' button on the home page is hard to see so I made it CO Sun yellow instead.

**Odds & Ends**

Some weird items include some data/graph tables and highlighted paragraphs. You can find these items in the following articles [Jared Polis campaign spending...](https://coloradosun.com/2018/09/14/jared-polis-campaign-spending-governor-race-2018/) & [Amid drought...](https://coloradosun.com/2018/09/12/colorado-water-law-drought-climate-change/) respectively.

I imagine these items will be more prevalent as more content is produced. I suspect some will even produce bugs. For example the table/graph is targeted by the following code.

{{< highlight css >}}
iframe[src*="//datawrapper"] {
	background-color: rgba(255, 255, 255, 0.7);
}
{{< /highlight >}}

As more content is produced this might need to be expanded, fixed and/or tweaked.

### That's all folks

Below you'll find some screenshots as well as the GitHub repository where this theme is stored. And now I should probably make my blog dark, eh?

**How to use**

You should be using the browser add-on [Stylus](https://add0n.com/stylus.html). Do **not** use Stylish as it has security issues. For reference, [Stylus on GitHub](https://github.com/openstyles/stylus).

[Stylus for Firefox](https://addons.mozilla.org/en-US/firefox/addon/styl-us/) - this works on the mobile version too!

[Stylus for Chrome](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne?hl=en)

Next, you can simply go to [Userstyles.org](https://userstyles.org/styles/164524/the-colorado-sun-dark-theme) and get it [directly](https://userstyles.org/styles/164524/the-colorado-sun-dark-theme).

Alternatively, the [CO Sun dark CSS file](https://github.com/obscuredetour/dark-co-sun/blob/master/co-sun-dark.css) can be copy/pasted into  the browser extension [Stylus](https://add0n.com/stylus.html) or click the **Raw** button to download. For reference here is the [Colorado Sun Dark theme on GitHub](https://github.com/obscuredetour/dark-co-sun).

### Screenshots


{{< figure class="image fit" src="https://github.com/obscuredetour/dark-co-sun/raw/master/screenshot-homepage.jpg" >}}
{{< figure class="image fit" src="https://github.com/obscuredetour/dark-co-sun/raw/master/screenshot-article.jpg" >}}