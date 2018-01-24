---
layout: post
title: Scholarly
thumbnail-path: "img/scholarly.png"
short-description: Scholarly is a vocabulary learning tool featuring quizzes and word suggestions.

---

{:.center}
!["A Scholarly quiz in action"]({{ site.baseurl }}/img/scholarlyquiz.png)

## Words, Words, Words
---
When I picked up my **summer readings** in 2017, I found myself in that all-too-familiar place of skimming over paragraphs and **not understanding the words** on the page.

> "What is *ignominy*? A *pedagogy*? How about a *platitude*? A *solecism*?"

I had the intent to **actually understand** what it was I was spending my time reading.

So I took out my **notebook** and started **writing down the words I didn't know** and looking up their definitions.

## A Practicality Issue
---
> "So this guy carried a notebook around with him and studied vocabulary words in his spare time?" *-- healthily skeptical person*

Not even once, actually.

Turns out the only time I had my notebook in front of me was when I was in the cafe where I was--you guessed it--**reading my book**.

Oh, and also still not knowing what was being said.

I needed a **better way** to **integrate these words** into my reading vocabulary.

## An App For That
---
> *"Surely there's an app somewhere for that."*


Yeahh, maybe. But I'm a **developer**. I already had the tools I needed to make this happen, so why not give it a shot?

Sure, there was probably **already an app out there** that did **99%** of what I wanted **and ran my dry cleaning** to boot.

*But this way,* I thought, *I get to make it my own. And who knows? Maybe that **1%** difference might be kinda cool.*

Either way, I stood to learn something.

## First Attempts
---
![]({{ site.baseurl }}/img/scholarlyproto.png)

This was one of my **first attempts** at **Scholarly**. Fundamentally, it had two parts:
  1. Add words to your vocabulary
  2. Take quizzes on a random sample of those words to test your memory

It had a couple issues, though.

Alright.. It had a lot of issues:

> *The interface to **add words** was a bit* clunky*.*

I asked a couple of friends to sit down and **if I didn't give them any instructions**, it **wasn't clear to them** how to use the app.

> *I thought **user metrics** would be a cool way to encourage the user to make progress in his or her learning.*   

In the end, though, I **couldn't find enough meaningful metrics** to display to the user at all times that didn't feel like **bloating** the app.

I ended up only keeping how well users were doing for any given word.

> *Although it still seems like a cool idea, **community notifications** was a leap too far into the app's future; it never made it to the finished product.*   

To encourage users to take on new words, I wanted users **to see the words the Scholarly community** was trying to learn.

In this version, you could click on words in the notifications to add them to your vocabulary.

This came with **unintended consequences**, though: users might feel **limited** to adding words they **didn't feel self-conscious** about.

I could have added settings to keep their words private.

Ultimately, I decided that in an app starting with **no users**, this **wasn't the ideal way for users to take on new words**.

And this realization was inconvenient, because...

> *You had to type in your words and **look up your own definitions**.*

**You had to do a lot of the legwork yourself.**

Aren't these newfangled tech gadgets supposed to make life easier?

> *Not to mention this is what it looked like on mobile.*

{:.center}
![]({{ site.baseurl }}/img/scholarlyprotomobile.png)

Ugh.


## Lessons Learned 

![Scholarly today]({{ site.baseurl }}/img/scholarly.png)

What you see above is **today's iteration** of **Scholarly**: the culmination of past lessons.

I still have a long way to go in my journey of becoming a better web developer, but **Scholarly taught me some early lessons**:

> Just because you already know how your app is supposed to work, doesn't mean your users will.

So design **intuitive** interfaces, **prototype** them early, and get **user feedback**.

Their reception of an idea is more important than your enthusiasm for it.

> This! And then that! But also find a place for this!

Sometimes **more is less**.

You know you've made something elegant not when you've added things left and right, but when you can no longer remove anything.

> Make sure what you're making will be useful to someone.

Adding **[Words API](https://www.wordsapi.com/docs)** to **Scholarly** *transformed* the app.

I used to keep a google tab open just to add words into **Scholarly**, but I found myself asking, *"**How convenient was this anyway?**"*

Now you can type in a word and **get a list of definitions** for the word you want. And if you don't see the one you want, you can **make your own**.

![Adding a Word]({{ site.baseurl }}/img/scholarlyaddword.png)

I've gone a step further and added **word suggestions** based on the words you've already added (an idea I can credit to my mentor).

All these quality of life improvements made this app **actually worth using**.

> Design the app for its intended use case.

Since my first iterations of **Scholarly**, I've rebuilt it from scratch using a **mobile-first design** approach.

I'm proud to say it's come a loong way since the first time I viewed my creation in Chrome DevTools.

{:.center}
![Scholarly (mobile)]({{ site.baseurl }}/img/scholarlymobile.png)

Of course I **still wonder** how I can make small changes to **improve the app** (or if more drastic ones still elude me).

But for now, I'm chasing after other ideas.

In the meantime, I'm adding words on the run and quizzing myself on my commute.

**And I've ditched the notebook**.

---
For the scholarly:
  * **ignominy** : (n.) a state of dishonor
  * **pedagogy** : (n.) the activities of educating or instructing; activities that impart knowledge or skill
  * **platitude** : (n.) a trite or obvious remark
  * **solecism** : (n.) a socially awkward or tactless act

---

You can check out **Scholarly** at [scholarly.cc](http://scholarly.cc).

**GitHub**: https://github.com/devonbahary/scholarly

**Thanks for reading!**
