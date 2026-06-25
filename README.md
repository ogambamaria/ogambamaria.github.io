# your site title

A minimal Jekyll site for blog posts and project write-ups, built for GitHub Pages.

## Structure

```
_posts/        blog posts (markdown)
_projects/     project write-ups (markdown)
_layouts/      page templates
_includes/     reusable snippets (sidebar nav)
assets/css/    stylesheet
index.html     home page (recent posts + projects)
blog/          blog index
projects/      projects index
about/         about page
```

## Writing a blog post

Create a file in `_posts/` named `YYYY-MM-DD-slug.md`:

```markdown
---
title: "My post title"
date: 2026-06-25
tags: [python, notes]
---

Your content here, in regular Markdown.
```

## Adding a project

Create a file in `_projects/your-project.md`:

```markdown
---
title: "Project name"
stack: [python, flask, postgres]
repo: "https://github.com/you/repo"
demo: ""
---

Description of the project, in Markdown.
```

Leave `demo: ""` empty if there's no live link.

## Site settings

Edit `_config.yml` to set:
- `title` — your site name, shown in the sidebar
- `tagline` — small line under the title
- `description` — used for the homepage intro and SEO
- `author.name` — shown in the footer
- `url` — your GitHub Pages URL once you know it, e.g. `https://yourusername.github.io`

## Running locally

Requires Ruby and Bundler.

```bash
bundle install
bundle exec jekyll serve
```

Then visit `http://localhost:4000`.

## Deploying to GitHub Pages

1. Push this repo to GitHub.
2. In the repo settings, go to **Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. Push to `main` — the included workflow (`.github/workflows/jekyll.yml`) builds and deploys automatically.

If you're using a **project page** (i.e. `https://yourusername.github.io/repo-name`, not a `username.github.io` repo), set `baseurl: "/repo-name"` in `_config.yml`.

## Removing the sample content

Delete the two files in `_posts/` and the one in `_projects/` once you've added your own.
