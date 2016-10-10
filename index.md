---
layout: page
title: CBB752 Spring 2017
tagline: Final Project
---
{% include JB/setup %}

## About the Course

**Title:** Bioinformatics: Practical Application of Data Mining & Simulation

-   **Instructor:** [Gerstein, Mark](<http://www.gersteinlab.org>)

-   **TAs**: [Huang, Xiu](http://xiu-huang.com) & [Lee, Donghoon](http://hoondy.com)

-   **Introduction:** Bioinformatics encompasses the analysis of gene sequences,
    macromolecular structures, and functional genomics data on a large scale. It
    represents a major practical application for modern techniques in data
    mining and simulation. Specific topics to be covered include sequence
    alignment, large-scale processing, next-generation sequencing data,
    comparative genomics, phylogenetics, biological database design, geometric
    analysis of protein structure, molecular-dynamics simulation, biological
    networks, normalization of microarray data, mining of functional genomics
    data sets, and machine-learning approaches to data integration.

-   Check out our awesome [course website](<http://cbb752b16.gersteinlab.org>).

-   Check out our [post on bioinformatics](<{% post_url 2016-4-10-Categories-of-knowledge-for-bioinformatics-education %}>).


## About the Final Project

- **Why?**

   Instead of generating papers or codes that nobody would ever read (expect for the TAs), we want to encourage the innovative generation of products that could potentially benefit the bioinformatics community.

- **When?**

    Released: April 14th

    Due: May 9th 11:59PM

- **How?**

    Each student will coorporate with classmates to work on three (or four for extra credits) different projects. The generated codes and documents will be published on this website to be resources for later students and researches.

- **What?**

    Project topics are as following. Students can choose three to four favorite projects to work on.

### For each sub-project, a group of three people will work on:

1.  **R card**: sample input, source code in R, sample output, and documentation on
    how to execute your code

2.  **Python card**: sample input, source code in Python, sample output, and
    documentation on how to execute your code

3.  **English card**: methodology and background introductory documentation

### Topics and Grouping Assignment

In `_config.yml` remember to specify your own data:
    
    title : My Blog =)
    
    author :
      name : Name Lastname
      email : blah@email.test
      github : username
      twitter : username

The theme should reference these variables whenever needed.
    
## Sample Posts

This blog contains sample posts which help stage pages and blog data.
When you don't need the samples anymore just delete the `_posts/core-samples` folder.

    $ rm -rf _posts/core-samples

Here's a sample "posts list".

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## To-Do

This theme is still unfinished. If you'd like to be added as a contributor, [please fork](http://github.com/plusjade/jekyll-bootstrap)!
We need to clean up the themes, make theme usage guides with theme-specific markup examples.


