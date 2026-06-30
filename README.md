# DealerOS Commerce Platform — Documentation

Engineering reference for the DealerOS Google Commerce stack: feed ingestion, Merchant Center provisioning, Google Ads/GBP integration, and the v2 Commerce Cockpit.

Built on [Mintlify](https://mintlify.com). Published at `commerce.dealeros.co/docs`.

## Local preview

Requires the [Mintlify CLI](https://www.npmjs.com/package/mint):

```bash
npm i -g mint
```

Run from the repo root (where `docs.json` lives):

```bash
mint dev
```

Preview at `http://localhost:3000`.

## Validate before pushing

```bash
mint validate      # strict — exits non-zero on warnings
mint broken-links  # checks all internal and external hrefs
```

Both must pass clean before merging to `main`.

## Pages

| File | Description |
|------|-------------|
| `index.mdx` | Platform overview |
| `onboard-a-dealer.mdx` | Step-by-step dealer onboarding |
| `architecture-overview.mdx` | System architecture |
| `feed-ingestion-pipeline.mdx` | Inventory feed → GMC pipeline |
| `data-model-and-schema.mdx` | Core data model and DB schema |
| `google-integrations.mdx` | Merchant Center, Ads, GBP, GSC wiring |
| `v2-cockpit-architecture.mdx` | v2 Commerce Cockpit (MUI + Motion) |
| `onboarding-and-setup-walkthrough.mdx` | Guided-manual setup flow |
| `source-to-normalization-to-gmc-tsv.mdx` | Feed normalization and TSV spec |
| `engineering-standards-and-conventions.mdx` | Coding and testing standards |
| `glossary-and-domain-model.mdx` | Domain glossary |

## Adding a page

1. Create `your-page.mdx` with a `title` and `description` frontmatter block.
2. Add the slug to the appropriate group in `docs.json` under `navigation.tabs[0].groups`.
3. Run `mint validate` and `mint broken-links` locally.
4. Open a PR against `main`.

## Resources

- [Mintlify docs](https://mintlify.com/docs)
- [docs.json reference](https://mintlify.com/docs/settings/global)
