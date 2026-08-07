# Wentao Wu — Academic Homepage

This repository is a lightweight academic homepage built with Jekyll and GitHub Pages, following the content organization used by [Academic Pages](https://github.com/academicpages/academicpages.github.io): site-wide configuration in `_config.yml`, navigation in `_data/`, Markdown pages in `_pages/`, and publications as a Jekyll collection in `_publications/`.

## Repository name

For the organization homepage, use:

```text
Vehicle-AHU/Vehicle-AHU.github.io
```

The expected site URL is:

```text
https://vehicle-ahu.github.io/
```

## Deploy

1. Create a **public** repository named `Vehicle-AHU.github.io` under the `Vehicle-AHU` organization.
2. Upload/push all files in this repository to the `main` branch.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **GitHub Actions** as the source.
5. The included `.github/workflows/pages.yml` workflow will build and deploy the site.

## First edits to make

Edit `_config.yml` and fill in:

- `author.email`
- `author.googlescholar`
- `author.orcid`
- `author.linkedin` (optional)

Replace `images/profile.svg` with a real portrait, for example `images/profile.jpg`, then update:

```yaml
author:
  avatar: "/images/profile.jpg"
```

## Add a publication

Create a Markdown file in `_publications/`, for example:

```markdown
---
title: "Paper Title"
year: 2026
authors: "Wentao Wu, ..."
venue: "Conference or Journal"
paperurl: ""
codeurl: ""
projecturl: ""
---

Short abstract or project description.
```

The Publications page will update automatically.

## Local preview

If Ruby and Bundler are installed:

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://127.0.0.1:4000`.

## License

The custom content and styling in this repository are provided under the MIT License. The site architecture is inspired by the open-source Academic Pages project.
