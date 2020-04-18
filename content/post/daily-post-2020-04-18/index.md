---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Daily Post - April 18, 2020"
subtitle: ""
summary: ""
authors: ["Ben Bigelow"]
tags: ["books","daily","Bokeh","Flask","Jinja"]
categories: []
date: 2020-04-18T18:23:39-04:00
lastmod: 2020-04-18T18:23:39-04:00
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

Well, you can't say that making data visualizations isn't tedious. Which is a statement that uses an Orwellian double negative and should really be written: making data visualizations is tedious.

I spent a good 2-3 hours today trying to make a decent visualization of variation in hospital markup rates using Bokeh. I ended up with a combination of a box-and-whisker chart and a categorical scatter plot with a jitter offset. Jitters are underrated, but I also tend to overuse them. In this case, though, it's a good way of letting users interact with the data - specifically, the hospitals with the highest charge-to-cost ratios - and contrast that with the average markup across the US. There's probably a better visualization out there, but at a certain point you need to say "Screw it" and commit your code.

## What I'm reading

Still plugging through _King Leopold's Ghost_ by Adam Hochschild. For all the evil Leopold II did in the world, you have to admire the man's political adeptness. Buying off lawyers, explorers, and journalists, wining and dining foreign diplomats and functionaries, anything to keep the gravy train (rubber steamboat?) flowing. 

Probably the crown jewel of Leopold's machinations was the way he buried a damning review of the realities of life in the Congo Free State written by an independent tribunal he himself sent to the Congo. Solution: have the report written in French, but send a sterilized and summarized version in English for circulation among the British and American press. Of course, eventually journalists figured out that the summary had nothing to do with the actual content of the report, but they had already run with the "All Quiet on the Congolese Front" version of events.

Moral of the story: if you don't want people to figure out what you're doing, bury it in an extensive government report filled with anodyne, bureaucratic mumbo-jumbo. Any normal person will be asleep by page 3.

## What I'm learning

Kept on with the Flask course. Learning some new stuff about inheritance in Jinja templates. I still don't fully understand the difference between the `{% block x %}` statement and the `{% include "x.html" %}` statement. Obviously has to do with inheritance, but when should you use one and not the other?

That said, I need to go refactor my own Jinja templates to use the `{% block title %}{% endblock %}` pattern to allow for different webpages to have different titles.