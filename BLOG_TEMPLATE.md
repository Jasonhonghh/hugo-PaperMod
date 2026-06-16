# Blog Template Layer

This branch packages the reusable presentation layer used by `dev-insight.cloud`
on top of PaperMod.

## Included

- Compact home list layout.
- Activity stream partials.
- Books list and book detail templates.
- Bilibili shortcode.
- Custom TOC, footer, post meta, sidebar partials.
- Extended CSS for typography, monochrome theme, home, books, activity, TOC,
  sidebar, top link, and mobile refinements.

## Site Data Expected

The theme reads these optional site data files when present:

- `data/activity.yaml`
  - Used by `layouts/partials/activity_stream.html`.
  - Expected to contain `last_updated` plus platform activity lists such as
    `github`, `douban`, `bilibili`, and `weread`.
- `content/books/*.md`
  - Used by the `books` section layouts.
  - Important front matter fields include `bookId`, `weread_url`, `author`,
    `cover.image`, `publisher`, `category`, `rating`, `intro`,
    `reading_progress`, `read_time`, `note_count`, `review_count`,
    `highlights`, and `notes`.

Data fetching is intentionally not bundled into the theme. Keep sync scripts
and GitHub Actions in the site repository so credentials and user-specific
sources stay outside the shared theme.
