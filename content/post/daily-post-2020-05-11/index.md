---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Daily Post - May 11, 2020"
subtitle: ""
summary: ""
authors: ["Ben Bigelow"]
tags: ["awk"]
categories: []
date: 2020-05-11T22:48:00-04:00
lastmod: 2020-05-11T22:48:00-04:00
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

Today I picked up an `awk` course that I dropped several months back. I've been thinking about revisiting it to develop a Unix version of some of the utilities in `csvkit`, which I tend to use on a regular basis. 

`csvkit` provides great descriptive summaries of tabular data, but it infers data types and structures in order to load the data into `pandas` dataframes. This can cause issues, particularly with numeric string data (e.g. years) and datetimes, if you're interested in what those fields _actually_ look like in the file, rather than the "pretty" version.

I'm curious to see how easy it would be to configure an `awk` script to summarize some data and output the results in a Bootstrap template. Could make reporting a breeze!