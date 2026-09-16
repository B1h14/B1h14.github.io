# Personal website — Bahaeddine Abdessalem

Built with [Jekyll](https://jekyllrb.com/) and the [Minimal Light](https://github.com/yaoyao-liu/minimal-light) theme,
hosted on GitHub Pages.

## Where things live

| File | What it controls |
| --- | --- |
| `_config.yml` | Name, position, affiliation, email, social links, avatar, favicon, SEO |
| `index.md` | About Me, Research Interests, News — and the order of the page sections |
| `_data/publications.yml` | The publication list |
| `_includes/experience.md` | Experience section |
| `_includes/projects.md` | Selected projects, awards, technical skills |
| `assets/img/avatar.jpeg` | Profile picture |
| `assets/files/` | CV PDF and any other downloadable files |
| `_layouts/`, `_sass/`, `assets/css/` | Theme internals — you rarely need to touch these |

## How to update the site

1. Edit the relevant file above.
2. Commit and push:
   ```bash
   git add -A
   git commit -m "Update news section"
   git push
   ```
3. GitHub rebuilds the site automatically. It's live in ~1 minute.

### Adding a publication

Append an entry to `_data/publications.yml`:

```yaml
  - title: "Paper Title"
    authors: <strong>Bahaeddine Abdessalem</strong>, Co Author
    conference_short: NeurIPS          # badge shown on the teaser image
    conference: Conference name and year.
    pdf: https://arxiv.org/abs/XXXX.XXXXX
    code: https://github.com/...       # optional
    page: https://project-page.com     # optional
    bibtex: https://...                # optional
    notes: Oral Presentation           # optional, shown in red
    image: ./assets/img/teaser.png     # optional
```

Entries appear in the order they're listed.

### Adding your CV

Drop the PDF at `assets/files/curriculum_vitae.pdf`, then uncomment the `cv_link`
line in `_config.yml`. Note that the LaTeX source contains a phone number — it is
gitignored on purpose. Check the compiled PDF before publishing it.

### Previewing locally (optional)

Requires Ruby. Install from [rubyinstaller.org](https://rubyinstaller.org/) (pick the
Ruby+Devkit version), then:

```bash
gem install bundler jekyll
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000. Pushing without a local preview is fine too.
