# Edgell Lab Website

Jekyll-based lab website for the Edgell Lab at Western University.

## Updating Content

All content updates are made by editing files in `_data/`:

- **`_data/news.yml`** — Add/remove news items
- **`_data/publications.yml`** — Add new publications
- **`_data/people.yml`** — Add/remove lab members

## Setup (first time)

1. Install Ruby and Jekyll: https://jekyllrb.com/docs/installation/
2. Run `bundle install` in this directory
3. Run `bundle exec jekyll serve` to preview locally at http://localhost:4000

## Deploying to GitHub Pages

```bash
git add .
git commit -m "Update site"
git push origin main
```

GitHub Pages will automatically rebuild and deploy the site.
