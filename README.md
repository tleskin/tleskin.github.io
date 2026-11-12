# Tom Codes

Personal blog by Tom Leskin, at [tleskin.github.io](https://tleskin.github.io).
Built with [Jekyll](https://jekyllrb.com/) on GitHub Pages, using a
custom theme written for this site (layouts in `_layouts/`, includes in
`_includes/`, styles in `_sass/` + `assets/css/main.scss`). No gem, no
`remote_theme` — everything the theme needs lives in this repo, so it
builds on the classic GitHub Pages branch build.

## Writing a post

Add a Markdown file to `_posts/` named `YYYY-MM-DD-slug.md`, with front
matter like:

```yaml
---
layout: post
title: "Your Post Title"
date: 2026-11-12 12:00:00 -0500
description: "One-line summary, used for the page description."
---
```

Push to `master` and GitHub Pages rebuilds the site automatically.

## Previewing locally

```sh
bundle install   # first time only; generates Gemfile.lock
bundle exec jekyll serve
```

Then open <http://localhost:4000>. The `Gemfile` pins the same
`github-pages` gem version GitHub Pages builds with, so the local
preview matches production.

## Notes

- The theme uses a dark teal background, sea glass accents, and a wide homepage
  hero. Its teal workspace image and Tom's cropped portrait live in `assets/img/`.
- Journal cards use `card_image:` or `image:` from a post's front matter.
  Posts without either get a styled cover. The homepage search filters
  visible posts in the browser.
- The sidebar's "Nerd stuff" tags come from `interests:` in `_config.yml`.
- The `resume` and `recommendations` pages are from 2015 and not linked
  in the header navigation. They still exist at `/resume/` and `/rec/`.
