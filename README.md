# Leonidas Christos Karagkounis — academic website

Personal academic website built with Jekyll and hosted on GitHub Pages at <https://karagkounisl.github.io/>.

## Site structure

- `_layouts/home-academic.html`: home page (bio, news, photo and links). `_pages/about.md` only sets its URL.
- `_data/news.yml`: dated news items on the home page, newest first.
- `_pages/research.html`: thesis and research interests.
- `_pages/cv.md`: CV, including a short third-person bio.
- `_pages/teaching.html`: teaching (from `_data/teaching.yml`) and service (from `_data/service.yml`, shown only when it has entries).
- `_pages/publications.html`, `_pages/talks.html`: filled from `_data/publications.yml` and `_data/talks.yml`. They appear in the navigation only once their data file has entries.
- `assets/css/academic.css`: all styling. A book-like design after Tufte CSS, set in EB Garamond, with light and dark themes.
- `_layouts/default.html`: header, footer and the theme toggle.

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
# _data/news.yml
- date: "Oct 2026" # shown as written
  text: "One sentence, first person."
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
