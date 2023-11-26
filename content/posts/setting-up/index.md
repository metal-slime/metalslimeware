+++
title = 'Setting Up'
date = 2023-11-24T16:49:26-06:00
draft = false
tags = ['hugo', 'install']
+++

## Setting Up metalslimeware.com

I've been a software engineer for a while now. I started out on this path as another bright eyed youngster, filled with joy at making things. As I've grown and developed, I had a lot of help from those who came before me and those on the journey with me. As I get older, I find joy in mentoring and helping those new young (or just young at heart) folks on their journeys.

To help me on that goal, I figured it was time I started to record my struggles, triumphs, and conundrums. That's where this blog comes in. But, before I could start writing on a blog, I had to have a blog.

## Every journey begins with a single step

Everyone starts new things up in their own way. Some dive right in and just start swimming. Others like to get their floaties on and slowly get into the water. I like to know how many bodies of water exist before I get in one. So, as I do, I asked my friends what they would use to self-host a blog. I was met with a resounding don't. Use something like [hugo](https://gohugo.io/) and [netlify](https://www.netlify.com/). I said, that sounds like a good idea and started looking at static site generators and frameworks.

I'm primarily a JavaScript developer these days so I was at first drawn to Eleventy and Astro. After reading a bit about them, both seemed like promising choices. I thought there could be one major problem with choosing either of these choices, though. If I picked a technology that was based on a language I was familiar with, I would be tempted to dive down into rabbit holes I didn't really need to. I didn't want to taint my new project with potential burnout from too many deepdives to I moved on.

Well, what else can I look at? Continuing on reading through choices I decided to take a look at Gatsby, Jekyll, and finally, hugo. In the end, I decided that trying out hugo would be a good place to start. It seemed to be lightning quick, had a lot of choices for templating, and just seemed like a fit for what I was aiming today. Everything said it should be easy to just install and go. I would see whether that was a true statement or not.

---

### Intermission

<font size="2">For those people who don't know me yet, I figured I could explain some of the design choices of the site. I'll do these throughout the site as little breaks from what we're doing because, well, it is fun for me and I hope for you!

Since I already wasted valueable Intermission space, I love JRPG's. Since I got my first copy of Dragon Warrior (Quest for you folks not in the US) through a Nintendo Power subscription gift I received at a bery special Christmas, I've been in love. Slimes were the first bad guy I fought, and as metal slimes are the embodiment of the JRPG grind, which I love, I've adopted them as a persona of sorts. But don't worry, 悪いスライムじゃないよ。</font>

---

## Let's try hugo

First, let me say, all of the site generators I looked at have fantastic guies and sites. hugo's is no exception to this. I went to the [Quick Start](https://gohugo.io/getting-started/quick-start/) page and started the install process. I would like to say I went to the Install page, opened up the macOS instructions and started building everything from scratch. I would like to say that, but that would be a lie. Instead, I took advantage of those who have come before me. A simple `brew install hugo` later, and I was ready to go. I made a new directory, `git init`ed, set my theme to (blowfish)[https://blowfish.page/], crossed my fingers, and one `hugo server` later, there everything was. 

"Look at that," I thought, it just worked. This really is simple. Am I done? Well, I was right, it was simple. It was running. But, I was wrong about one thing. I was not done. I was just getting started.
