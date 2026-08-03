# nextcraft.github.io

Next Craft organization site — mission front page plus wiki (projects, members, blog). Hosted on GitHub Pages.

## Local development

```bash
bundle install
bundle exec jekyll serve -d /tmp/nextcraft-site -H 127.0.0.1 -P 4000
```

Open [http://127.0.0.1:4000](http://127.0.0.1:4000).

> If the repo lives on OneDrive / cloud sync, build with `-d /tmp/nextcraft-site` (or another local path). Writing `_site` into the synced folder can fail with `Errno::ECANCELED`.

## Structure

| Path | Role |
|------|------|
| `index.html` | Org front page (2026 AI-oriented) |
| `about.md`, `members/`, `projects/`, `_posts/` | Wiki / archive content |
| `blog.html` | Post index |
