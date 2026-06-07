# Lucas Layton — Photography Portfolio

Personal photography portfolio and blog, built with [Hugo](https://gohugo.io) and hosted on GitHub Pages.

Live site: https://tubs12.github.io/photography_website/

---

## Running locally

```bash
hugo server
```

The site is available at `http://localhost:1313`. It live-reloads on any file change.

---

## Adding photos

1. Drop image files (`.jpg`, `.png`, `.webp`) into `assets/photos/`
2. That's it — Hugo picks them up automatically and optimizes them at build time

Photos appear in the grid on the homepage in filesystem order. To control the order, prefix filenames with numbers: `01-portrait.jpg`, `02-landscape.jpg`, etc.

---

## Writing a blog post

Create a new `.md` file in `content/blog/`:

```bash
hugo new content blog/my-post-title.md
```

Or just create the file manually. The filename becomes the URL slug (`my-post-title` → `/blog/my-post-title/`).

Every post needs this front matter at the top:

```markdown
---
title: "My Post Title"
date: 2026-06-07
description: "One sentence shown on the blog listing page."
draft: false
---

Your content here.
```

- Set `draft: true` to write without publishing. Run `hugo server --buildDrafts` to preview drafts locally.
- Standard Markdown works: `**bold**`, `*italic*`, `# headings`, `[links](url)`, `![images](path)`, code blocks, etc.

### Publishing

Push to `main` and GitHub Actions deploys automatically:

```bash
git add content/blog/my-post.md
git commit -m "Add new post: my post title"
git push
```

The site updates in about 30 seconds.

---

## Editing site details

Open `hugo.toml` to change your name, tagline, or description:

```toml
[params]
  author = "Lucas Layton"
  tagline = "Photography & Writing"
  description = "Photography portfolio and personal blog"
```
