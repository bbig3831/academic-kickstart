---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Daily Post - April 28, 2020"
subtitle: ""
summary: ""
authors: ["Ben Bigelow"]
tags: ["Flask", "Python", "daily", "books", "HTML"]
categories: []
date: 2020-04-28T21:52:26-04:00
lastmod: 2020-04-28T21:52:26-04:00
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

Oy! Who knew that forms were so difficult? My _Extreme Markup_ project is nearing completion, and the last real page to fix up is the **Contact** page. Turns out you can write client-side validation with HTML types and the `required` keyword for `input` fields, server-side validation with some Python class shenanigans, AND you then have to set up the configuration with a mail server to send the e-mails for you.

I tried playing around with Flask-WTF after watching some tutorials, but I wasn't really a fan. Ditto for Flask-Bootstrap. Even if they both come with some nice handling for forms, there doesn't seem to be an easy way to configure CSS classes so that the form style matches the rest of the site. Additionally, at least for Flask-Bootstrap, you have to pass your Flask app as a parameter into a `Bootstrap()` object, which obscures things a little too much for my taste. Looks like we're sticking to generic Flask and Python for this one.

## What I'm learning

Ditto above, how to send an e-mail via a contact form with Flask. I went back to the _Talk Python_ Flask course I've been going through, and the section on the View-Model design pattern was quite useful, even though I didn't quite understand it. Seems like it's a way of encapsulating data in Flask for your Jinja templates in order to keep things cleaner than just passing huge dictionaries or numerous keyword parameters.

## What I'm reading

_The Bonfire of the Vanities_. There's a definite subtext of envy to the novel. You can tell by the green motif that crops up a number of times, even though I'm only ~180 pages into the 700 page book. There's green in Sherman McCoy's apartment; Maria's building is colored "rental unit green"; and Lawrence Kramer's Bronx courthouse has "government office green". Everybody wants something they don't have, because what they have isn't what they want.