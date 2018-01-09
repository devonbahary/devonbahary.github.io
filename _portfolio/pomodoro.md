---
layout: post
title: Pomodoro
thumbnail-path: "img/pomodoro/pomodoro-demo.png"
short-description: Pomodoro is a time management tool used to improve your work flow.

---

{:.center}
!["Pomodoro - A time management tool"]({{ site.baseurl }}/img/pomodoro/pomodoro-demo.png)

## The Technique (Explanation)
---
Last year a friend and I got to talking about the **best methods we'd found for tackling the day's challenges and getting things done**.

There's so many things that **compete for our attention**. How can we best **optimize the time** we have in a way that respects the entirety of our needs?

That's when he brought up the **[Pomodoro Technique](https://en.wikipedia.org/wiki/Pomodoro_Technique)**. It was **simple**:
  * Set yourself **goals** for your work session
  * **Work for 25 minutes**. No distractions.
  * Take a **5 minute break**.
  * (Repeat the above 4 times, taking a **30 minute break** after your 4th completed work period.)

The **Pomodoro Technique** is **strict**, in that there are discrete periods of time where I **don't get to reach for my phone or watch that unrelated video**.

But it's also **understanding**, because it allows me time twice an hour to do those things **guilt-free**.

It keeps me **accountable** because I only permit myself to wander away from my work **after I've put meaningful time** into it. Even then, I have to be cognizant of how long I wander.

The **Pomodoro Technique** became a valuable study asset during my web development education at **[Bloc](https://www.bloc.io)**.

## When Given The Option, Build Something Useful (Problem)
---
Imagine my enthusiasm when I saw a Pomodoro app among the list of project electives at the end of the curriculum.

![A suggested wireframe for the Bloc Pomodoro project]({{ site.baseurl }}/img/pomodoro/bloctime-wireframe.png)


It called for a few things:
  * **Task creation** in an interface
  * Task **persistence** through **[Firebase](https://firebase.google.com/docs/)**
  * Feature to mark and distinguish tasks as **complete**
  * Use of **Angular's** `$interval` service to simulate a timer
  * Implementation of the **[Buzz sound library](http://buzz.jaysalvat.com/documentation/buzz/)** to play a timer ding

Easy enough! Let's get to it!

## Finished, But Not Complete (Solution)
---
![Pomodoro Prototype]({{ site.baseurl }}/img/pomodoro/pomodoro-proto.png)

This is the project I ended up submitting.

I had a couple of **design goals** in mind with this project:

> One of the takeaways [I wrote about in building my Scholarly app]({{ site.baseurl }}/portfolio/scholarly) was to design intuitive interfaces and reduce unnecessary content in my future development.

Off the bat I knew **this project didn't require a lot going on**, so I knew **the interface should reflect its minimalist ambitions**:
  * The background is both calm yet slick. It provides a relaxed ambience while communicating intent.

---
  * An empty **task pane** hovers over left. It doesn't have content yet, but **it didn't need to dominate an entire hemisphere** of the interface with a container background just to **communicate** that it can.

---
  * The timer has **one button**. A second button appears when the timer is running, but not otherwise.

{:.center}
![Timer reveals second button]({{ site.baseurl }}/gif/pomodoro/timer-reveal.gif)

---
  * Your work state is reflected by a combination of **icons and color**. With an art style with so much gray, I thought this subtle contrast **communicated a lot with little**.

{:.center}
![Pomodoro Icons]({{ site.baseurl}}/img/pomodoro/pomodoro-icons.png)

---

I met the requirements of the project in good time, though not without underestimating the snags I would run into along the way (a lesson that is becoming quite apparent to me through web development).

**But it wasn't yet the app I wanted to use**. In this version:
  * You could add tasks and mark them complete, but there **wasn't a way to dismiss finished tasks altogether**.
  * There was **only one set of tasks being recorded in the database**: enough for only one person using the tool, but **not to be of use to a broader user base**.


## One More Time With Enthusiasm (Results)
---

Since submitting the project, I've added **several more features** to the app:

---

> Tasks can now be destructed.

{:.center}
![Task Resolution]({{ site.baseurl }}/gif/pomodoro/task-resolution.gif)

---
> You can sign up to keep a personal list of tasks over multiple sessions.

{:.center}
![Personal Tasks]({{ site.baseurl}}/img/pomodoro/pomodoro-in-action.png)

If you're visiting as a guest, you won't share a common database of tasks by everybody like in the first version.

Tasks are **yours alone**--they just won't save for next time.

> I thought there was real value on offer to retain tasks over multiple sessions, so I wanted to encourage user sign-up.

{:.center}
![Profile button collapsing]({{ site.baseurl }}/gif/pomodoro/profile-collapse.gif)

A **sign-in prompt** floats into the user's screen on page load and gently **retracts into the profile icon if the user doesn't interact with it**; I respect that the user understands he or she can sign in and knows where to do so.

{:.center}
![Pomodoro User Sign-Up]({{ site.baseurl }}/gif/pomodoro/signup.gif)

Once the user has decided to sign in or sign up, I wanted the process to be as **clean** and **intuitive** as possible.

---

> I wanted it to be abundantly clear to the user what the app was offering and how to use it.

{:.center}
![Pomodoro Help Modal]({{ site.baseurl }}/img/pomodoro/pomodoro-help.png)

A **help modal** can be summoned by a button at the bottom corner of the page with **explanations** for the handful of icons the user will interact with in the app.

Even with this addition, though, I felt that there was **still an obstacle between my app and potential users**.

After all: what good was an app that helped them do something they weren't even **knowledgeable** about?


---

> I wanted the app to **introduce itself** to guest users--especially those unfamiliar with the Pomodoro Technique.

{:.center}
![Pomodoro Greeting]({{ site.baseurl }}/gif/pomodoro/pomodoro-greeting.gif)

{:.center}
![Pomodoro Instruction]({{ site.baseurl }}/img/pomodoro/instruction.png)

The app now extends a hand **as soon as the user loads the page**.

And it continues to do so throughout each first encounter in the Pomodoro process, **building the bridge between the user's understanding and its utility**.


## A Place For Pomodoro (Conclusion)

[I wrote about a few takeaways that I got from building my Scholarly app]({{ site.baseurl }}/portfolio/scholarly). They continue to sit with me **through my design process**, and there were a few that echoed through my designing of **Pomodoro**:

> Just because you already know how your app is supposed to work, doesn't mean your users will.

**At the risk of holding first-time users' hands**, I've **removed** the chance that visitors will glance at the work I've put into this app with a **blank stare**: the app will **literally walk you through** your first iteration of the Pomodoro Technique**.

Through the design process, I **chose icons with consideration** and exercised the use of **selective color to communicate to the user** what each feature does.

A help modal **summarizes interactions** with the app succinctly.

> This! And then that! But also find a place for this!

Pomodoro isn't chock-full with features and its purpose is for organization, so its design should offer a **decluttered, simplified environment**.

I think I accomplished creating components in the UI that don't take up more space than they need (some even **disappear** when not in use or only appear when they **can** be used).

The characteristics the components do have **convey what they're intended for**.


> Make sure what you're making will be useful to someone.

**Adding persistent tasks for signed-in users** was a big step in this direction.

**Tracking tasks over the long-term** makes the app feel a lot more like a **reliable to-do list** with the function of **facilitating accomplishing those goals in the near-term**.

I'm proud of how this one turned out, and yet again satisfied that I made something that can be of use to someone.

After all, I've used **Pomodoro** to write this case study.

---

**Thanks for reading!**
