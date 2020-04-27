---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Daily Post - April 26, 2020"
subtitle: ""
summary: ""
authors: ["Ben Bigelow"]
tags: ["Flask", "PythonAnywhere", "Python", "books", "daily"]
categories: []
date: 2020-04-26T21:00:06-04:00
lastmod: 2020-04-26T21:00:06-04:00
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

I didn't spend a whole lot of time today on my _Extreme Markup_ project, but the time I did spend on it was very productive. I decided to finally get things set to deploy the Flask app on PythonAnywhere, which is a Python cloud service. Time to let my baby fly free on the web.

Overall, the deployment process was pretty straightforward, starting with an `ssh-keygen` to get an SSH key to use with GitHub and then a quick `git clone` to copy my repo over. 

Next up was the virtual environment. PythonAnywhere has several out-of-the-box, but I found out through trial-and-error that I needed to build one custom: at the very least, the `bokeh` package that _Extreme Markup_ uses was several versions ahead of the one in PythonAnywhere's Python 3.6 environment.

This is where things got hairy. Apparently, the memory quota on PythonAnywhere is fairly limited, so running `pip install -r requirements.txt` - especially with the Jupyter notebook packages - maxed out that space. I ended up going through the "really required" packages one by one to get them installed without hitting the memory threshold. Tedious, to say the least. But at last, after one final `pip install pandas==1.0.2`, the site was live! Huzzah! I've put a password on it for now until I'm done cleaning things up, but not bad for an hour of work.

## What I'm learning

Today I learned that I'm having trouble settling on a book. I thought about spending some time on the Talk Python Flask course, but I need to spend less time on the computer, so I'm going to kick back until tomorrow.

## What I'm reading

I got about 50 pages into _Vicksburg, 1863_ before giving up. I'll come back to it later, but I'm just not in the mood for heavy historical non-fiction. (Although I did enjoy the chapter on Ulysses S. Grant's fall and rise into his command in the West prior to the Vicksburg campaign.)

So, I packed that in quietly and moved my bookmark over to Tom Wolfe's _The Bonfire of the Vanities_. I've never read anything by him, although his verbosity has been referred to in several things I have read. (Most recently, actually, _Joe Gould's Secret_.) So far, I see the prolixity, but it doesn't make the book feel hefty. You can breeze through twenty or thirty pages pretty quickly given the casual nature of his prose.

## What I'm thinking about

I'd like to write a compare/contrast with the way major media outlets covered protests leading up to the Iraq war - such as the ANSWER protest in DC - with the way they covered the Women's Marches across the US in the wake of Donald Trump's election in 2016. From some initial digging into _NYT_ archives, the conclusion seems self-evident, but I'd like to be more thorough about it.