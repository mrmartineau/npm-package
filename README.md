# npm-package-base

A small, reusable starter repo for building TypeScript npm packages with ESM, CJS output, declaration files, Biome, and `release-it`.

This repository is meant to be copied and customized for each new package you publish. It now contains only generic starter code and setup.

## What's included

- TypeScript source in `src/`
- Bundling with `tsup`
- ESM + CommonJS output in `dist/`
- Generated `.d.ts` types
- Linting and formatting with Biome
- Release workflow via `release-it`

## How to use this template

1. Create a new repository from this one, or clone/copy it into a new folder.
2. Update `package.json`:
   - change `name`
   - change `description`
   - set the initial `version`
   - update `license`, `repository`, `homepage`, and `bugs` fields if you want them
   - remove `"private": true` before publishing
3. Replace the starter implementation in `src/index.ts` with your package code.
4. Add any runtime dependencies your package needs.
5. Install dependencies and start developing.

## Install dependencies

```bash
bun install
```

## Starter API

The current starter export is intentionally minimal:

```ts
import { hello } from 'your-package-name'

console.log(hello())
console.log(hello('team', { punctuation: '!!' }))
```

Replace this with your actual public API once you start the new package.

## Development

```bash
# Build ESM, CJS, and type declarations
bun run build

# Rebuild on file changes
bun run dev

# Check & fix formatting + linting
bun run check
```

## Project structure

```text
.
├── src/
│   └── index.ts
├── dist/
├── biome.json
├── package.json
└── tsconfig.json
```

## Publishing checklist

Before publishing a package created from this template:

1. Replace the starter code in `src/index.ts`.
2. Update `package.json` metadata.
3. Run `npm run build`.
4. Run `npm run check`.
5. Publish with your preferred workflow, for example `npm publish` or `npm run release`.

## Notes

- The template targets Node.js 20+.
- Package entrypoints are exposed through the `exports` field.
- Build output is written to `dist/`, which is the only published directory.

## License

[ISC](https://choosealicense.com/licenses/isc/) © [Zander Martineau](https://zander.wtf)

> Made by Zander • [zander.wtf](https://zander.wtf) • [GitHub](https://github.com/mrmartineau/)
