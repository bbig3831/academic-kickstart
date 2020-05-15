---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "PDF book bashing"
subtitle: ""
summary: ""
authors: ["Ben Bigelow"]
tags: ["bash", "programming"]
categories: []
date: 2020-05-14T20:52:54-04:00
lastmod: 2020-05-14T20:52:54-04:00
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

At the start of the coronavirus pandemic, Project MUSE began allowing free downloads of books from a number of different publishing companies and universities, like Johns Hopkins Press, University of North Carolina Press, etc. I perused some of the offerings and found a number of books of interest, particularly books on healthcare and health policy. Unfortunately, you have to download book sections - cover page, table of contents, chapter 1, and so on and so forth - **_one at a time_**. Tedious, to say the least.

I could've written a Python script to scrape the pages and download the PDFs, but it was only about 10-12 books, not really worth the time to get frustrated with `BeautifulSoup` and `requests`, given my basic knowledge of those libraries. So download the PDFs one by one I did.

But THEN what I discover is that the PDFs all have a cover page. Every. Single. One. PDF of the cover is two pages, cover page and actual cover. Chapter 2? Cover page _and then_ chapter 2. Oy!

Knowing that there was probably a quick and programmitic solution to my problems, I discovered the PDF toolkit `pdftk` and wrote a short `bash` script to remove the cover pages of all these PDFs and then combine them to create the entire manuscript. 

```bash
for dir in */ ; do
    # Trim directory name
    dir=${dir%*/}
    echo "Combining PDFs for $dir" ;
    mkdir "$dir/trimmed" ;
    echo "Trimming PDFs for $dir"

    # Trim cover page from all PDFs and save in "trimmed" directory
    for pdf in "$dir"/*.pdf ; do
        output=$(basename "$pdf") ;
        pdftk "$pdf" cat 2-end output "$dir/trimmed/$output" ;
    done ;
    # Concatenate trimmed PDFs
    pdftk "$dir/trimmed"/*.pdf cat output "$dir.pdf" ;
    echo "Done combining PDFs for $dir" ; 
    echo "Removing trimmed directory" ;
    rm -R "$dir/trimmed" ;
    echo "" ;
done ;

echo "Finished combining all PDFs" ; 
exit 0 ; 
```

Nothing to it. I'm still a little vague on variable expansion, but it got the job done and that's all that matters.

[Link to gist](https://gist.github.com/bbig3831/d4ed2a969260073d242d115cd465f82d)