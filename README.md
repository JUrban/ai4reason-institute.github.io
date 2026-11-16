# ai4reason.eu

Website of the AI4REASON Institute (AI4REASON z.ú.), served by GitHub Pages at <https://ai4reason.eu>.

## Deploying

The site is plain Jekyll, built by GitHub Pages itself, with only Pages-supported plugins
(`jekyll-feed`, `jekyll-seo-tag`, `jekyll-sitemap`, `jekyll-redirect-from`). There is no build
step and no GitHub Action: **push to `main` and Pages rebuilds the site** (Settings → Pages →
“Deploy from a branch”, `main`, `/ (root)`). `CNAME` keeps the custom domain.

## Editing

| What | Where |
|---|---|
| News | `_posts/YYYY-MM-DD-slug.md`, with `title` and a one-sentence `description` in the front matter |
| People, visitors | `_data/people.yml` (photos in `assets/img/people/`, 360×360 JPEG, metadata stripped) |
| Publications | `_data/publications.yml` (`group`: `paper`, `talk` or `manuscript`; `people` drives the filter) |
| Research projects | `_data/projects.yml` |
| Addresses, email, navigation | `_config.yml` |
| Pages | `index.html`, `about.md`, `research.html`, `publications.html`, `people.html`, `news.html`, `funding.html`, `contact.html`, `annual-report-2025.md` |
| Styles | `assets/css/site.css` (one file; colours follow the annual report, dark mode is automatic) |

Old URLs (`/people.html`, `/news.html`, `/sponsors.html`, `/veroff-aim-proof.html`) redirect to
the new pages. The PDFs stay at the site root so that existing links keep working.

## Previewing locally (optional)

```bash
gem install bundler
bundle install        # uses the Gemfile (github-pages gem = the same versions as Pages)
bundle exec jekyll serve
```

Then open <http://localhost:4000>.
