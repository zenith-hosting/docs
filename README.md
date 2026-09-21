# Zenith developer docs

This repository guides developers through containerising an app, creating `zenith-compose.yml`, and submitting the app to Zenith.

The site is built with [Mintlify](https://mintlify.com). Pages are MDX files, and site configuration lives in `docs.json`.

## Sources of truth

- `../zenith/internal/xzenith/xzenith.proto` defines the public schema.
- `../zenith/internal/xzenith/validate.go` defines intrinsic validation.
- `../zenith/internal/kubernetes2/transform/validator.go` validates a full app proposal.
- `../zenith/internal/xzenith/ENV.md` defines environment resolution.

## Preview the site

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview your documentation changes locally. To install, use the following command:

```
npm i -g mint
```

Run the following command at the root of your documentation, where your `docs.json` is located:

```
mint dev
```

View your local preview at `http://localhost:3000`.

## Check a change

```bash
mint broken-links
mint validate
```
