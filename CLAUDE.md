# CLAUDE.md

Guidance for Claude Code (and other AI assistants) working in this repository.

## What this repository is

This is **build-your-own-x**, a curated, link-only list of step-by-step guides
for recreating well-known technologies from scratch (databases, shells,
regex engines, Docker, Git, etc.), maintained by CodeCrafters. There is no
application code, no build system, and no tests — the entire "product" is
the annotated list of external links in `README.md`.

## Repository layout

```
README.md                 # The list itself — all content lives here
ISSUE_TEMPLATE.md          # Template used when someone opens a submission issue
codecrafters-banner.png    # Banner image embedded at the top of README.md
.gitattributes             # Marks *.md as linguist-detectable, not documentation
```

There are no source directories, package manifests, CI config, or tests in
this repo. Do not go looking for (or try to add) a build/lint/test pipeline —
none is expected.

## Structure of README.md

1. **Banner + intro** — the CodeCrafters banner image and a short blurb.
2. **Table of contents** — an alphabetized bullet list of category anchors
   (`#build-your-own-3d-renderer`, `#build-your-own-database`, etc.), ending
   with `#uncategorized`.
3. **`## Tutorials`** — the body, one `####` subheading per category
   (`#### Build your own \`Database\``, etc.), each followed by a flat bullet
   list of entries.
4. **`## Contribute`** — how to submit/review new tutorials.
5. **`## Origins & License`** — CC0 dedication and attribution.

### Entry format

Each tutorial is a single bullet line of the form:

```
* [**Language**: _Tutorial Title_](https://url-to-tutorial) [optional-tag]
```

- **Language** is bold and comes first (e.g. `**Go**`, `**C++**`, `**(any)**`
  for language-agnostic tutorials, or `**Language1 / Language2**` when a
  tutorial covers more than one).
- *Tutorial Title* is italicized and matches the source's own title as
  closely as practical.
- The link goes directly to the tutorial/article/repo, not to a landing page.
- Optional bracketed tags follow the link for non-article formats, e.g.
  `[video]` or `[pdf]`.

### Ordering conventions

- Categories in the table of contents are alphabetical and link to matching
  `####` headers in the `## Tutorials` section — keep both in sync if you add
  or rename a category.
- Entries within a category are *roughly* alphabetized by language, but this
  is not strictly enforced historically — newly contributed entries are
  commonly appended to the end of their category's list rather than
  insertion-sorted. Match whichever convention the surrounding section
  already uses; don't mass-reorder an existing section as a drive-by change.
- The `Uncategorized` section is for tutorials that don't fit an existing
  category. If several uncategorized entries share a clear theme, that's a
  signal a new category (and TOC entry) may be warranted rather than more
  additions to `Uncategorized`.

## Contribution workflow (what a "task" usually is)

Most changes to this repo are one of:

1. **Adding a new tutorial** — append an entry (see format above) to the
   appropriate category section in `README.md`. If the category doesn't
   exist yet, add both a new `####` section and a corresponding TOC bullet
   (kept alphabetical among the other TOC entries).
2. **Fixing a broken/moved link** — update the URL in place; keep the
   language/title text unless the source itself renamed the tutorial.
3. **Editing wording** — minor corrections to titles, language tags, or
   category names.
4. **Reviewing submissions** — for issues opened via `ISSUE_TEMPLATE.md`,
   check the submission is a genuine step-by-step, build-it-yourself guide
   (not a framework/library doc, not a "glue two libraries together"
   tutorial) before turning it into a README entry.

When editing, make the smallest diff that accomplishes the task — this file
is large (~500 lines) and reviewed by humans as a plain diff, so avoid
reflowing or reordering unrelated lines.

## Content acceptance criteria

Per `ISSUE_TEMPLATE.md`, only accept/add tutorials that:
- Provide a guided, step-by-step path (either as a written article series or
  code broken into clearly digestible steps).
- Build something interesting **from scratch**.
- Are **not** framework/library documentation, framework/library tutorials,
  or tutorials that merely wire existing libraries together.

## License and attribution

The repository content is dedicated to the public domain under **CC0**
(see the `## Origins & License` section of `README.md`). Don't add content
that isn't compatible with that (e.g., don't paste in copyrighted tutorial
text — only link to it).
