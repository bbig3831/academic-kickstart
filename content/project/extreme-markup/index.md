---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Extreme Markup"
summary: ""
authors: ["Ben Bigelow"]
tags: ["Python", "Bootstrap", "Flask", "Bokeh", "PythonAnywhere"]
categories: []
date: 2020-03-28T20:04:25-04:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: "Smart"
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
_Extreme Markup_ is a paper replication project that allowed me to work on a broad range of stuff. The [original paper](https://www.healthaffairs.org/doi/full/10.1377/hlthaff.2014.1414) by Gerard Anderson and Ge Bai used Medicare Healthcare Cost Report Information System (HCRIS) files to analyze charge-to-cost ratios in the US. They identified the hospitals with the highest markups and presented data on their characteristics, such as ownership structure and location.

I built this project with a number of different tools:

* **HTML and CSS** - I don't have much front-end experience, so I used the [Bootstrap](https://getbootstrap.com/) framework to make things easy.
* **Flask** - The main web app is written in Python using the Flask micro-framework.
* **Bokeh** - [Bokeh](https://bokeh.org/) is a Python visualization library that provides some great utilities for making interactive visualizations for the web.
* **PythonAnywhere** - [PythonAnywhere](pythonanywhere.com/) is a cloud service for Python apps. Heroku seemed like overkill for what I needed and it doesn't provide support for SQLite databases.