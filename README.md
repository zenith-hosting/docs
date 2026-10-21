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

## Preview the site

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview your documentation changes locally. To install, use the following command:

```bash
npm i -g mint
```

Run the following command at the root of your documentation, where your `docs.json` is located:

```bash
mint dev
```

View your local preview at `http://localhost:3000`.

## Check a change

```bash
mint broken-links
mint validate
```
