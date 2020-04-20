---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Daily Post April 19, 2020"
subtitle: ""
summary: ""
authors: ["Ben Bigelow"]
tags: ["Bokeh", "daily"]
categories: []
date: 2020-04-19T22:22:31-04:00
lastmod: 2020-04-19T22:22:31-04:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
## What I'm doing

Today I did a fat lot of nothing, outside of binging Season 3 of _Fargo_. In my defense, I'm usually pretty good about managing my time. And also, coronavirus. And Sunday morning donuts and coffee. Can you blame someone for wanting to sit on the couch after that?

I did manage to get around to writing a Python function to classify hospitals based on their system affiliation, in order to match the categories in the _Extreme Markup_ paper I'm replicating. Very tedious. First, I thought I'd do it with a lookup table in my Postgres DB, then just add that as a column in my SQLAlchemy model/ORM. But since I only need it for the hosiptals with the highest markup, not every hospital, in each year, I figured I could just do it in `pandas` instead. Admittedly, this seems less "clean" than storing the values in the SQLite DB, but I'm really just trying to ship the Flask app at this point. I can refactor it later.

I also had to futz around with Bokeh's stacked area charts, which apparently don't have good `HoverTool` functionality yet. Who knew. So you have to hack it with a `vline_stack` in addition to your `varea_stack`.

Moral of the story: I really need to learn some good front-end data viz stuff. That way, I can at least have some more control over what I'm doing.

## What I'm learning

Also a fat lot of nothing. Hooray!

## What I'm reading

_King Leopold's Ghost_. And _Fargo_. It's basically like a book.

## What I'm thinking

How do you know when you're trying to rouse someone's moral outrage and when you just want someone to see how smart you are? There's been a number of conversations I've had in the past few weeks where, afterwards, I end up feeling like I trotted out a whole bunch of facts and anecdotes and research _just to be right_. To get someone to think the way I do. Which isn't a conversation, it's a tirade. A rant. 

When should you exercise self-control and when should you let your sense of moral imperative short-circuit niceties and social convention? I need to learn to walk back my tone and approach difficult or contentious conversations with a calmer demeanor. 