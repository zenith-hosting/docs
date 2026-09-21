# Zenith developer documentation instructions

## Project structure

- This is a Mintlify site.
- Pages are MDX files with YAML frontmatter.
- Configuration lives in `docs.json`.
- Use the Mintlify skill for component, configuration, and writing guidance when changing the site.
- In navigation, `zenith-compose.yml` is a group whose `root` is the main guide. Its only child page is titled `Reference`.

## Writing

- Write for developers integrating an app, not for Zenith's implementation team.
- Use active voice and second person.
- Keep sentences short. One idea per sentence.
- Use sentence case for headings.
- Put file names, commands, paths, fields, and configuration keys in code formatting.
- Prefer complete, runnable examples over fragments.
- State defaults, constraints, failure cases, and interactions between fields.
- Use "app" for the developer-facing package. Use "product" only when the implementation or API names it that way.
- Avoid marketing copy, filler, and undocumented promises.
- Use Mintlify `Visibility` blocks when web readers and Markdown-consuming agents need different instructions.
- Keep facts and schema reference shared outside `Visibility`. Do not duplicate a large reference solely to make an agent version.
- Put browser navigation, cards, and dashboard interaction in `for="humans"` blocks. Put agent task contracts, verification criteria, and authorization boundaries in `for="agents"` blocks.
- Use components for meaning, not decoration: `Steps` for ordered workflows, `Info` and `Note` for context, `Warning` for real risk or unsupported behavior, and `Check` for a verifiable completion state.
- Put paired navigation cards in responsive `Columns`. Keep core schema tables and validation rules visible instead of hiding them in accordions.

## Content boundaries

- Document the public Compose contract and the developer workflow around it.
- Do not expose secrets, private infrastructure, moderation internals, or operator-only configuration.
- Do not copy implementation details into the specification unless developers must rely on them.
- Mark unstable behaviour clearly. Omit it if there is no public compatibility commitment.
