---
author: firdausmubarik
comments: true
date: 2015-07-01 15:28:08+00:00
layout: post
link: http://firdausmubarik.com/2015/07/css-log-flexwrap-in-safari/
slug: css-log-flexwrap-in-safari
title: 'CSS Log: Flexwrap in Safari'
wordpress_id: 180
categories:
- Web Design
tags:
- css
- css3
- design
- flex
- web design
---

I got problems in one of our website: JAX.co.id recently. The body area of page in article is draggable to left. This found in Safari Maveriks, Yosemite doesn't react this way.

[![Screen Shot 2015-07-01 at 10.10.04 PM](http://firdausmubarik.com/wp-content/uploads/2015/07/Screen-Shot-2015-07-01-at-10.10.04-PM-1024x566.png)](http://firdausmubarik.com/wp-content/uploads/2015/07/Screen-Shot-2015-07-01-at-10.10.04-PM.png)

if i open one article like [jazz gunung](http://jax.co.id/jazz-gunung-2015-post-factum/) and swipe the trackpad there will empty space in the right of page.

I have two suspect: css flex or my implementation of parallax banner. After checking several article parallax is out of suspect, it also happened in article without parallax.

Then I open developer tools in Safari, and try to localize the problems. After deleting one by one several element I can identity the problems: newsletter subscription after article and in footer. Deleting that two eliminating the problems.

So my final suspect: FLEX. I use flex because it flexible to have element in right and left in certain width then giving the rest to center element. But flex is part of CSS3 new implementation that not really supported by all browser.

Checking in Cainisue.com i finally figuring out. I forget to give -webkit- prefix in [flex box](http://caniuse.com/#feat=flexbox).

css before


    
    form    
        +displayflex() //my custom flex with all prefix
        flex-wrap:  wrap // the problem 
        align-items: center



adding -webkit-flex-wrap: wrap fixing my draggable problem!

before:

[![Screen Shot 2015-07-01 at 10.09.37 PM](http://firdausmubarik.com/wp-content/uploads/2015/07/Screen-Shot-2015-07-01-at-10.09.37-PM-1024x568.png)](http://firdausmubarik.com/wp-content/uploads/2015/07/Screen-Shot-2015-07-01-at-10.09.37-PM.png)

after:

[![Screen Shot 2015-07-01 at 10.36.14 PM](http://firdausmubarik.com/wp-content/uploads/2015/07/Screen-Shot-2015-07-01-at-10.36.14-PM-1024x576.png)](http://firdausmubarik.com/wp-content/uploads/2015/07/Screen-Shot-2015-07-01-at-10.36.14-PM.png)














