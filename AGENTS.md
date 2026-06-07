# Documentation project instructions

## About this project

- This is the customer-facing Babbily help center built on Mintlify.
- Pages are MDX files with YAML frontmatter.
- Configuration lives in `docs.json`.
- Use Mintlify components such as `Card`, `CardGroup`, `Steps`, `AccordionGroup`, `Note`, `Warning`, and `Tip` when they make a page easier to scan.

## Terminology

- Use **Babbily** for the product.
- Use **Saved Prompts** for custom reusable assistants. Do not use internal shorthand in customer docs.
- Use **API usage budget** for plan usage. Do not call it tokens or credits.
- Use **Memory Profile** for the customer-visible memory summary.
- Use **Connectors** for connected apps.
- Use **Skills** for reusable instructions and workflows.
- Use **Temporary Chat** for private, unsaved chat mode.
- Use **Library** for saved chats, translations, and media.

## Style preferences

- Write in second person: "you can," "your chat," "your workspace."
- Use active voice and concise sentences.
- Use sentence case for headings.
- Bold UI labels: Click **Settings**.
- Use `>` between UI locations: **Settings > Memory**.
- Prefer customer tasks and outcomes over implementation details.
- Include short examples when they help a customer take action.

## Content boundaries

- Explain visible behavior, controls, limits, plan effects, privacy expectations, and troubleshooting steps.
- Do not expose internal database table names, private route paths, environment variables, service-role behavior, secrets, implementation-only logs, hidden cron behavior, or provider wiring details.
- Do not claim unsupported guarantees. If behavior can vary by model, plan, connector, or account state, say so.
- Do not document internal admin features or operations-only runbooks.
- Keep external provider names out of customer docs unless the provider is visible in the UI or needed to explain customer trust, authorization, or billing.

## Verification

Before shipping, run:

```bash
mint validate
mint broken-links --check-anchors --check-redirects --check-snippets
mint a11y
```

Preview with:

```bash
mint dev --no-open --port 3000
```
