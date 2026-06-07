# Babbily Help Center

This repository powers the customer-facing Babbily documentation site.

The site is built with [Mintlify](https://www.mintlify.com/docs). Pages are MDX files, and navigation, branding, and global settings live in `docs.json`.

## Local preview

Install the Mintlify CLI, then run the preview from this repository root:

```bash
pnpm add -g mint
mint dev --no-open --port 3000
```

Open `http://localhost:3000` to review the docs locally.

## Validation

Run these checks before opening or updating a pull request:

```bash
mint validate
mint broken-links --check-anchors --check-redirects --check-snippets
mint a11y
```

## Writing standards

- Write for customers, not internal implementers.
- Use second person and active voice.
- Use Babbily UI labels exactly as they appear in the product.
- Explain visible behavior, limits, privacy expectations, and user controls.
- Do not document internal tables, private endpoints, environment variables, secrets, service-role behavior, implementation-only logs, or hidden provider wiring.

## Publishing

Make changes on a feature branch and open a pull request. Mintlify preview deployments should be used for review before merging to `main`.
