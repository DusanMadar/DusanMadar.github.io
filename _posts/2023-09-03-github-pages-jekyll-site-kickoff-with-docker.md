---
layout: post
title:  "GitHub Pages Jekyll site kickoff with Docker"
excerpt: >
  After struggling to start a Jekyll site, I finally found a solution that
  simplifies bootstrapping a Jekyll GitHub Pages site with Docker.
---


**tl;dr** [github-pages-jekyll-site-kickoff-with-docker](https://github.com/DusanMadar/github-pages-jekyll-site-kickoff-with-docker)


# Motivation

So I've decided to start a blog. You know, to occasionally share my thoughts,
ideas, and experiences. I wanted to use something simple, ideally a self-hosted
solution which supports writing posts in Markdown.

Somewhat naturally (I've been using GitHub for years), the decision fell on
[GitHub Pages](https://pages.github.com/); their landing page mentions Jekyll.
I've never used Jekyll before, but why not, let's give it a try.

Turns out it's not exactly trivial to get started. Especially for someone with
zero experience with the Ruby ecosystem.

# Jekyll site bootstrap and Docker

My mindset is to use Docker for everything. I don't want to install anything
on my machine, but rather run it in a container. There are a few Docker images
and/or blog posts about running Jekyll in Docker. Though I wasn't able to get
any of them to bootstrap a new site.

[How to use Develop Jekyll (and GitHub Pages)
locally using Docker containers](https://github.com/BillRaymond/my-jekyll-docker-website)
was uncovered after some digging and it claims the following:

> There are so many variables in getting it right, that many people give up in
frustration.

My thoughts exactly. Permission issues, missing dependencies, you name it.
I have had some progress with producing a Gemfile and even running the site.
However, it was mostly a lucky combination of a handful of commands and I
wasn't able to reproduce the process end-to-end.

## GitHub Pages Jekyll site kickoff with Docker

It all finally clicked after hours of trial and error and compiling information
from various source. A quick and dirty bash script and a docker-compose.yaml
file for convenience that make the job done are available in a repository which
aims to be **a helper to create an empty Jekyll site for GitHub Pages
with Docker**:
[github-pages-jekyll-site-kickoff-with-docker](https://github.com/DusanMadar/github-pages-jekyll-site-kickoff-with-docker).


### Credits

- [Docker Compose and Jekyll](https://urre.me/writings/docker-compose-and-jekyll/)
  - the aforementioned docker-compose.yml is based on the one from this blog
- [How to use Develop Jekyll (and GitHub Pages) locally using Docker containers](
https://github.com/BillRaymond/my-jekyll-docker-website)
  - it's quite detailed and covers a lot of related topics, but it's a great
  read if you want to understand how the whole thing works
- [Creating a GitHub Pages site with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)
