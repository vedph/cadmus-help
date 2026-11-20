# Cadmus Help

User documentation and reference manual for Cadmus. 🔗 URL: <https://vedph.github.io/cadmus-help/>.

## Documentation structure

- individual part editors are documented in files named after their TYPE ID (see <https://vedph.github.io/cadmus-doc/models/shared.html>).
- reusable UI components ("bricks") are documented under `bricks/`.
- documentation images are stored under `img/` in its parent folder (`bricks` images go into `bricks/img`). If they are screenshot, name them after the last part of the type ID + a 2-digits numeric suffix (e.g. `note01.png`).
- links to images and internal documentation should use relative paths.

## Conventions

- 🔑 component or part ID
- ⚠️ warning
- 🚩 technical term or definition
- 💡 tip
- ▶️ procedural step
- 👉 important information
- 🎯 purpose
- 📚 [thesaurus](https://vedph.github.io/cadmus-doc/linking/thesauri.html) ID

## Authoring features

- **code**: use fenced code blocks with a language for syntax highlighting (Rouge), e.g. ` ```json `. A copy button is added automatically.
- **diagrams**: use a ` ```mermaid ` fenced block to render a [Mermaid](https://mermaid.js.org) diagram.
- **images**: images in page content can be clicked to zoom (unless they are wrapped in a link or are SVG).
- **navigation**: pages nested at the third level (e.g. `bricks/*.md`, `parts/*.md`) need both `parent` and `grand_parent` in their front matter.

## Local preview

Requires Ruby and Bundler:

```sh
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000/cadmus-help/>.

## Publishing

In the GitHub repository settings, under **Pages**, set the source to *Deploy from a branch*, branch `main`, folder `/ (root)`.
