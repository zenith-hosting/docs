# Zenith developer docs

This repository guides developers through the Zenith CLI: preparing an app, testing a temporary deployment with `zenith up`, and submitting a public GitHub commit with `zenith publish`.

The site is built with [Mintlify](https://mintlify.com). Pages are MDX files, and site configuration lives in `docs.json`.

## Sources of truth

- [Zenith CLI](https://github.com/zenith-hosting/zenith-cli) defines the commands, preview checks, and publishing workflow.
- `content/quickstart.mdx`, `content/up.mdx`, and `content/publish.mdx` cover the main developer workflow.
- Agent instructions live in `Visibility for="agents"` blocks and `docs.json`. Use `NO_COLOR=1` for plain CLI output, with explicit inputs for non-interactive sessions.
- `../zenith/internal/xzenith/xzenith.proto` defines the public schema.
- `../zenith/internal/xzenith/validate.go` defines intrinsic validation.
- `../zenith/internal/kubernetes2/transform/validator.go` validates a full app proposal.
- `../zenith/internal/xzenith/ENV.md` defines environment resolution.
- `../zenith/contract/zenith-compose.schema.json` defines the public JSON Schema.
- `../zenith/contract/zenith-dev-compose.schema.json` adds preview source-build constraints.
- `../zenith/internal/devpublish/artifacts.go` defines publish builds and preview image reuse.

## Preview the site

Install the [Mintlify CLI](https://www.npmjs.com/package/mint):

```bash
npm i -g mint
```

From the repository root, start the preview:

```bash
mint dev
```

View your local preview at `http://localhost:3000`.

## Check a change

Validate the site and check internal links:

```bash
mint broken-links
mint validate
```
