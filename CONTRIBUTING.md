# Contribute a post to bkb.sh

bkb.sh is a blog of thoughts and experiments in building software. Posts live here,
in the open, so anyone can propose one with a pull request — no access to the blog's
code required. This is an **experimental** pipeline; expect the odd rough edge.

## Add a post in 4 steps

1. **Fork** this repo and create a branch.
2. **Add** `posts/<your-slug>.md` with this frontmatter:
   ```yaml
   ---
   title: "Reading Postgres EXPLAIN like a detective"
   description: "One line — used on cards and link previews."
   date: 2026-07-13            # YYYY-MM-DD
   tags: ["postgres", "sql"]   # optional
   author: your-handle         # must match a key in authors.json
   ---

   Body is Markdown. Use `##` headings; fenced code blocks get highlighting.
   ```
3. **Add yourself** to [`authors.json`](authors.json) (skip if you're already there):
   ```json
   "your-handle": {
     "name": "Your Name",
     "github": "https://github.com/your-handle",
     "social": { "label": "x", "url": "https://x.com/your-handle" }
   }
   ```
   `social` is one link of your choosing — X, a personal site, LinkedIn, wherever
   you'd like readers to find you. `label` is the short text shown next to it.
4. **Open a pull request.** Once it's merged into `main`, the post is built into
   bkb.sh and credited to you, linking to your GitHub and your `social`.

## Guidelines

- Write from real work — things you built, broke, or figured out. Not tutorials
  copied from elsewhere.
- Keep it yours: only submit writing you have the right to publish.
- One post per PR keeps review simple.
- Topics that fit: web, backend and APIs, microservices, data and messaging, cloud
  and DevOps — anything about building and running software.

## What happens after merge

The blog pulls this repo's `posts/` and `authors.json` at build time. A merge to
`main` triggers a rebuild, and your post goes live within minutes.
