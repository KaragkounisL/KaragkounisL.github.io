# Leonidas Christos Karagkounis — academic website

Personal academic website built with Jekyll and hosted on GitHub Pages at <https://karagkounisl.github.io/>.

## Site structure

- `_pages/about.md` and `_layouts/home-academic.html`: homepage and research overview.
- `_pages/cv.md`: academic CV, education, experience, and training.
- `_pages/research.html`: doctoral research and research interests.
- `_pages/publications.html`: publications, populated from `_data/publications.yml`.
- `_pages/talks.html`: conferences and talks, populated from `_data/talks.yml`.
- `_pages/teaching.html`: teaching and service, populated from `_data/teaching.yml` and `_data/service.yml`.
- `_pages/portfolio.html`: projects page. New projects can be added here when ready.
- `assets/css/academic.css`: compact site design and responsive styling.
- `_layouts/default.html`: shared header and footer.
- `_config.yml`: site metadata and profile links.

The previous template's sample blog posts, publications, talks, teaching entries, and projects have been removed. Empty Publications, Talks, and Teaching pages are ready but hidden from the main navigation until entries are added. Current research repositories are private and are not presented as public projects.

## Add academic entries

Each `_data/*.yml` file starts as `[]`. Replace that line with a YAML list. Omit optional fields that do not apply. Link to a publisher or conference page whenever possible.

```yaml
# _data/publications.yml
- title: "Paper title"
  authors: "A. Researcher, L. C. Karagkounis"
  venue: "Journal or conference name"
  year: 2026
  type: "Journal article" # or Conference paper, Preprint, Book chapter
  doi: "10.0000/example" # optional, without https://doi.org/
  url: "https://example.org/paper" # optional
  pdf: "/files/paper.pdf" # optional, local PDF
  code: "https://github.com/example/repository" # optional
  note: "Award or other brief context" # optional
```

```yaml
# _data/talks.yml
- title: "Presentation title"
  date: 2026-06-15
  type: "Conference talk" # or Poster, Invited talk, Workshop
  event: "Event name"
  location: "City, Country"
  description: "One-sentence summary" # optional
  url: "https://example.org/event" # optional
  slides: "/files/slides.pdf" # optional, local PDF
  video: "https://example.org/video" # optional
```

```yaml
# _data/teaching.yml
- course: "Course title"
  role: "Teaching assistant"
  institution: "University name"
  term: "Spring 2026"
  description: "Brief description" # optional
  url: "https://example.org/course" # optional
```

```yaml
# _data/service.yml
- title: "Program committee member"
  organization: "Conference name"
  year: 2026
  type: "Reviewing"
  description: "Brief description" # optional
  url: "https://example.org/conference" # optional
```

These examples are documentation only; they do not appear on the site.

## Local preview

With Ruby and Bundler installed:

```sh
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000/>. GitHub Pages also builds the site from the repository after changes are pushed.
