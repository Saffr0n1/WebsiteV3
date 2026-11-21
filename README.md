# Abi Panday

Personal homepage at **https://abipanday.com**. Plain HTML and CSS, a locally
hosted Hack font, and two PDFs. No JavaScript, dependencies,
package manager, or build step.

## Edit and preview

Edit `index.html` for content and `css/style.css` for appearance. From this
directory:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000. Stop the server with Ctrl+C.

The résumé is a committed public snapshot, not a live link to private notes.
After rebuilding it in the sibling `resume` project, refresh it with:

```sh
cp ../resume/output/pdf/resume.pdf documents/resume.pdf
```

The thesis is `documents/thesis.pdf`. The header's thotbot link opens the
separate thotbotglitched blog; it is not built or managed here.

The Penrose-triangle icon's vector source is `assets/favicon.svg`. Checked-in
exports include a 32px PNG, a 180px Apple touch icon, and `favicon.ico` with
16px, 32px, and 48px sizes. Both HTML pages declare the same icons.

## Publish

Commit and push to `main`. GitHub Pages publishes the repository root
automatically. `.nojekyll` tells Pages to serve these static files directly.
`404.html` is the custom missing-page response. The previous site is available
in Git history; its pages and redirects are not part of this version.

GitHub Pages uses `abipanday.com` as its custom domain, with HTTPS enforcement
enabled. Keep `CNAME` set to that domain. Squarespace manages the DNS records
and permanent forwarding from `abishrantpanday.com`; ordinary content updates
do not require DNS or forwarding changes.

Hack is bundled locally; its license is included in `assets/fonts/LICENSE.md`.
The homepage is served at `/`, with no `.html` in navigation or public links.
If adding a page, use a directory with an `index.html` (for example,
`about/index.html` for `/about/`).
