# Tom Codes

Personal blog by Tom Leskin, at [tleskin.github.io](https://tleskin.github.io).
Built with [Jekyll](https://jekyllrb.com/) on GitHub Pages, using the
[Minima](https://github.com/jekyll/minima) theme (v2.5.1 — the version
GitHub Pages ships).

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

- The theme is Minima 2.5.1 (not v3, and not Chirpy): both of those need
  Jekyll 4 / a GitHub Actions build, and this repo still uses the classic
  GitHub Pages branch build. If the repo ever moves to an Actions build,
  the theme can be revisited.
- Styling tweaks live in `assets/main.scss` (variable overrides before
  the `@import "minima"` line, plus a few extra rules after it).
- The `resume` and `recommendations` pages are from 2015 and not linked
  in the header navigation. They still exist at `/resume/` and `/rec/`.
