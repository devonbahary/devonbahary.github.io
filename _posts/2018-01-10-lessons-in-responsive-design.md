---
layout: post
title: Lessons In Responsive Web Design
---

## Growing Pains

Imagine packing for a vacation. You have all these ideas of what to bring.

So many ideas!

You know everything will have to fit into your smaller suitcase, but just to gather everything together you throw what you'll be bringing into your larger suitcase first.

You'll find a way to fit it in the smaller suitcase later!

Except, that's a bad idea. That's not going to work.

I have a confession guys... I kind of did this.

## Let's Just Say It Was My First Vacation

If you saw **[the case study of my Scholarly project]({{ site.baseurl }}/portfolio/scholarly)**, you might recall that my first iteration of **[Scholarly]({{ site.baseurl }}/portfolio/scholarly)** was built **without mobile-first design** principles.

For a demonstration of why this is a **bad** practice, check out this face-palm moment I had the first time I rendered the app I was building in a **mobile view**.

{:.center}
Not bad at first, right?

![An early version of Scholarly]({{ site.baseurl }}/img/scholarlyproto.png)

{:.center}
But then...

{:.center}
![Ouch]({{ site.baseurl }}/img/scholarlyprotomobile.png)


**Yikes**..

## I Couldn't Squeeze Everything Into The Smaller Suitcase

While I was designing **[Scholarly]({{ site.baseurl }}/portfolio/scholarly)** on my laptop screen, it felt like **each component** in the view occupied a **logical space** and was **functional** there.

But on a **mobile screen**, each component was **squished** to a width that made it **illegible** and **unusable**.

This design error was most egregious in the **header bar** at the top of the view. Notice the difference between the two buttons in the top-right corner in the **original view** and in the **mobile view**.

I wasn't even reluctant to start over. **After reading a few articles and watching a couple videos on responsive web design**, I had new insights that got me excited to do it right.

## The Result Is Much Improved

{:.center}
Finished product, large screen

![Scholarly now]({{ site.baseurl }}/img/scholarlydisplay.png)

{:.center}
And on mobile screens

{:.center}
![Scholarly, this time with responsive design]({{ site.baseurl }}/img/scholarlymobiledisplay.png)

---
### How To Pack A Small Suitcase
> Stack elements on top of each other in mobile views.

Rather than try to squeeze half the components on one side of the mobile view and half on the other side, I decided to **stack each component one on top of another**.

This gives each component element **the space** it and the user deserves for the user to **understand what's being presented** and **interact** with them.

> Intuitive symbols > verbose descriptions

To use space more efficiently, I **replaced** buttons that had **word descriptions** in them with buttons occupied by single **semantic icons**.

> If it doesn't fit, create a new view for it.

Uh, consider this taking advantage of side pockets in your suitcase.

For example, a **cumbersome *Add Word* button** in the first iteration of [Scholarly]({{ site.baseurl}}/portfolio/scholarly) has been **replaced** with a large, attention-grabbing **+ button** common in many of today's mobile applications.

This single button takes the user to a **separate view** where word management is more graceful, **focusing on new components** related to word searching and **away from the components irrelevant to that task**.

As the user scrolls down to view words at the bottom of the page, the button will disappear so as to not get in the way; it'll reappear on scroll-up.

If the user doesn't need to see it, it **doesn't need to clutter the screen**!

## Suitcase Packing Principles
> **Mobile-first**.

**Design everything in your app in a mobile view first**. It's much easier to broaden out and expand your UI than to find a place for everything to fit in a small space afterwards.

---
> Use **media breakpoints** to change the appearance of components in the app at different screen size intervals.

From my **[research online on responsive web design](https://developers.google.com/web/fundamentals/design-and-ux/responsive/#how_to_choose_breakpoints)**, I've come across some great guidelines to design with:

> TL;DR
>
> * Create breakpoints based on content, never on specific devices, products, or brands.
> * Design for the smallest mobile device first; then progressively enhance the experience as more screen real estate becomes available.
> * Keep lines of text to a maximum of around 70 or 80 characters.

A lesson worth mentioning is to **insert media queries** at screen sizes **relevant to your application**.

Catering your application to **adjust at intervals respective of independent devices** can feel **forced** and leads to a **"maintenance nightmare"** down the road when devices inevitably change.

---
### CSS Grid + Positioning

When stacking components in mobile, I've become fond of `display: grid`.

If you're unfamiliar with CSS Grid, here's a **[great intro](https://gridbyexample.com/video/series-define-a-grid/) from a tutorial site** and a **[lengthier talk](https://www.youtube.com/watch?v=txZq7Laz7_4)** that puts it into the greater context of web development.

As I developed **[Scholarly]({{ site.baseurl }}/portfolio/scholarly)** the second time around, I set a **parent container** to `grid` that held all the stacked components.

**From that parent container's CSS declarations**, I could **manipulate all its child components heights** within a **single line** of CSS using `grid-template-rows`.

{% highlight css %}

#view-container {
    display: grid;
    grid-template-rows: 20% 30% 50%; /* 3 components */
    width: 100vw;
    height: 100vh;
}
{% endhighlight %}

In your **media queries** at **larger screen widths**, you can set the **child containers** to `position: absolute` with appropriate `height` and `width` properties, using `top`, `right`, `bottom`, and `left` properties to **arrange them around the view**.


And that's it for this one!

---

You can check out **Scholarly** at [scholarly.cc](http://scholarly.cc).

GitHub: https://github.com/devonbahary/scholarly

**Thanks for reading!**
