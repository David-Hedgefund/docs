# David documentation

The documentation site for **David** — synthetic financial data API for building, training, and evaluating financial AI agents. Built on [Mintlify](https://mintlify.com).

## Structure

- `docs.json` — site configuration (branding, navigation, theme).
- `index.mdx` — the Introduction page.
- `quickstart.mdx`, `authentication.mdx`, `errors.mdx` — getting started.
- `concepts/` — core concepts (scenarios, synthetic data, coverage, ticker universe, date semantics).
- `guides/` — task-oriented how-tos.
- `api-reference/` — one page per endpoint group, documenting every endpoint.
- `logo/`, `favicon.svg` — brand assets.

Pages are MDX files with YAML frontmatter. Content is modeled on the structure of the Financial Datasets documentation and sourced from the SynthFin API (the engine behind David's synthetic data).

## Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint):

```
npm i -g mint
```

Run from the repo root (where `docs.json` lives):

```
mint dev
```

Preview at `http://localhost:3000`.

## Publishing

Install the Mintlify GitHub app from your dashboard to deploy on push to the default branch.

## Troubleshooting

- Dev server not running? Run `mint update` for the latest CLI.
- Page 404? Make sure you're in a folder with a valid `docs.json` and the page is listed in its `navigation`.

## Support

[investors@davidhf.com](mailto:investors@davidhf.com)
