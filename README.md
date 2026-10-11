# blog

Personal site/blog built with [Hugo](https://gohugo.io) using the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme (included as a git submodule).

## Setup

```bash
git submodule update --init --recursive   # fetch the PaperMod theme
brew install hugo                         # install Hugo, if needed
```

## Run locally

```bash
hugo server -D
```

Serves the site at `http://localhost:1313/` with live reload. `-D` includes draft posts.

## Writing a new blog post

```bash
hugo new content/blogs/my-post-title.md
```

This uses `archetypes/blogs.md` to pre-fill front matter and a basic outline:

```yaml
---
title: "My Post Title"
date: 2026-01-01
draft: true
author: "David Souza"
tags:
  - engineering
image: /images/post.jpg
description: ""
toc: true
---
```

Write the post under the generated `## Introduction` / `## Main Content` / `## Conclusion` headings (or replace them). Set `draft: false` when it's ready to publish.

## Adding a project

Projects live on a single page, not one file per project: edit `content/projects.md` and add a new entry following the existing pattern:

```markdown
### Project Name

A brief description of what this project does and the problem it solves.

**Tech:** Go, PostgreSQL, Docker

[View on GitHub](https://github.com/Davidsouza20) | [Live Demo](#)
```

## Build for production

```bash
hugo
```

Outputs the static site to `public/`.
