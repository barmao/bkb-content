---
title: "Contributing a post to bkb.sh"
description: "A sample community post — and a working example of how the contributor pipeline hangs together."
date: 2026-07-13
tags: ["meta", "writing"]
author: octocat
---

This post lives in the public [`bkb-content`](https://github.com/barmao/bkb-content)
repo, not in the (private) blog itself. It's here to prove the pipeline works: a
Markdown file with frontmatter, merged into `main`, shows up on bkb.sh with a byline
that links back to its author.

## Why a separate repo

The blog's code is private, but its **content** doesn't have to be. Keeping posts in
a public repo means anyone can propose one with a normal pull request — no access to
the application, no secrets, just words in a file.

## What a post needs

Nothing exotic — the same frontmatter any post uses, plus an `author` handle that
maps to an entry in `authors.json`:

```yaml
---
title: "Your title"
description: "One line for cards and previews."
date: 2026-07-13
tags: ["thing", "other-thing"]
author: your-handle
---
```

Write the body in Markdown, open the PR, and once it's merged the post is built into
the site — credited to you, linking to your GitHub and one other profile.
