# Tom Codes

Personal blog by Tom Leskin, at [tleskin.github.io](https://tleskin.github.io).
Built with [Jekyll](https://jekyllrb.com/) on GitHub Pages, using the
[So Simple](https://github.com/mmistakes/so-simple-theme) theme (v3.2.0,
installed as a `remote_theme`).

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

- The theme is So Simple 3.2.0 (not Chirpy or Minima v3): both of those
  need Jekyll 4 / a GitHub Actions build, and this repo still uses the
  classic GitHub Pages branch build. If the repo ever moves to an Actions
  build, the theme can be revisited.
- The skin is set in `_config.yml` (`skin: /assets/css/skins/default.css`
  — `light.css` and `dark.css` are the other built-in options). Custom CSS
  goes in `assets/main.scss`, which mirrors the theme's own file.
- The top navigation comes from `_data/navigation.yml` (the theme only
  renders the menu if that file exists).
- The `resume` and `recommendations` pages are from 2015 and not linked
  in the header navigation. They still exist at `/resume/` and `/rec/`.
