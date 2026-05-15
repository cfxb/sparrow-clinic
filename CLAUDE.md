# CLAUDE.md

Project guidance for Claude Code working on the Sparrow Neuropsychology website.

## Site basics

Static Jekyll site (Ruby 3.3.6, pinned in `.ruby-version`). Build with:

    eval "$(rbenv init - zsh)" && rbenv shell 3.3.6 && bundle exec jekyll build

Pages live at the repo root as `*.md` with `layout: page`; condition resources live under `resources/`. Shared partials are in `_includes/`, layouts in `_layouts/`, structured data in `_data/` (notably `navigation.yml` and `contact.yml`). `_site/` is gitignored.

## Standing rules

### Bump the FAQ "Last updated" date on every commit
The `_Last updated: YYYY-MM-DD_` line in `faq.md` must always reflect today's date in any pushed commit, even when the change is to an unrelated page. A pre-commit hook in `.githooks/pre-commit` does this automatically — **but only if `core.hooksPath` is configured on the clone.** Before working in a fresh clone, verify with:

    git config core.hooksPath

If that returns nothing or anything other than `.githooks`, run:

    git config core.hooksPath .githooks

### No medico-legal / forensic content
Dr. Benjamin does not currently provide medico-legal evaluations in BC. If user-provided drafts mention medico-legal, forensic, expert testimony, insurance-claims documentation, or related framing, strip or reword it and flag the change. ("BC Children's Hospital" as a hospital name is fine — that is not a service reference.)

### No pediatric assessment content
Dr. Benjamin does not do pediatric assessments. Avoid framing services or pages around children, pediatric assessment, or school-based assessment. Incidental clinical mentions like "onset in childhood" as an ADHD diagnostic criterion are fine; references to pediatric *services* are not.

## FAQ page specifics

`faq.md` carries the `faq_schema: true` front-matter flag, which causes `_includes/head.html` to inject `_includes/faq-schema.html` — the `FAQPage` JSON-LD schema — into `<head>`. **Any edit to a Q&A in `faq.md` must be mirrored in the corresponding `acceptedAnswer.text` (or `name`) in `_includes/faq-schema.html`,** or the page body and the schema will drift out of sync. The schema is what search engines and LLMs index, so divergence is a real problem.
