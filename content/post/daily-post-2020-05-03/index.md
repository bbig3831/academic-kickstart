---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Daily Post - May 3, 2020"
subtitle: ""
summary: ""
authors: ["Ben Bigelow"]
tags: ["Flask", "Python", "PythonAnywhere"]
categories: []
date: 2020-05-03T22:20:15-04:00
lastmod: 2020-05-04T22:20:15-04:00
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

Well, I had quite the day configuring my code to work with [PythonAnywhere](pythonanywhere.com/). Turns out, even _after_ I had installed all the packages I needed in my virtual environment, I was still getting 500 error codes for an internal server error. Error logs showed some sort of SMTP issue.

After scouring the internet, I stumbled on a help page in the PythonAnywhere forum with the answer. I guess that PythonAnywhere has a whitelist of IP addresses for a proxy for free accounts. Mail server requests can get blocked if they're not on the whitelist. Turns out, Microsoft's `smtp.office365.com` wasn't one of the good ones. Oh well, so I had pass my data over to Google, which ended up being supported on the platform. Minor bummer, but still.

## What I'm learning

I've learned all about SMTP crapola, I can tell you that much. I also made sure to properly configure my Flask app using a `.env` file that isn't commited to VCS. Then, you can use the `os` module in Python to load the environment variables defined in `.env` and build configuration classes.

I actually was pleasantly surprised by this pattern. Class inheritance makes it easy to set certain variables at the top, such as mail server parameters, which are then passed down to child classes. Class attributes are easy to use in most IDEs, too. 

The downside is that you have to remember what things are called between your `.env` configuration file and the configuration class attributes. 