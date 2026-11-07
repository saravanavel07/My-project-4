# My-project-4

A documentation website built with **Astro** and **Starlight**. It provides a clean, responsive foundation for publishing guides and reference material using Markdown and MDX.

[![Built with Starlight](https://astro.badges.dev/built-with-starlight.svg)](https://starlight.astro.build/)

## Project overview

This repository is currently based on the Starlight starter template. It includes a splash-style welcome page, an example guide, and an example reference page that you can replace with content for your project.

## Technology stack

- **Astro 5** — static site framework and development/build tooling.
- **Astro Starlight** — documentation theme, layouts, navigation, and built-in documentation features.
- **Markdown and MDX** — authoring formats for documentation pages; MDX also allows JSX components such as Starlight's `Card` and `CardGrid`.
- **TypeScript** — used for the Starlight content collection configuration.
- **Sharp** — image processing dependency used by Astro.

## Components and structure

| Path | Purpose |
| --- | --- |
| `src/content/docs/index.mdx` | Welcome/splash page. Uses Starlight's `Card` and `CardGrid` components to show next steps. |
| `src/content/docs/guides/` | Task-oriented documentation pages. Includes an example guide. |
| `src/content/docs/reference/` | Concise reference documentation. Includes an example reference page. |
| `src/content.config.ts` | Registers the Starlight docs content collection, loader, and schema. |
| `src/assets/` | Source assets used within pages; currently contains the welcome-page image. |
| `public/` | Static files served as-is, including the site favicon. |
| `astro.config.mjs` | Configures Astro, Starlight's site title, sidebar groups, and navigation. |
| `package.json` | Project scripts and dependencies. |
| `tsconfig.json` | TypeScript configuration. |

### Starlight UI components currently used

The home page imports and renders `Card` and `CardGrid` from `@astrojs/starlight/components`. Starlight also provides the overall documentation interface, including page layout and the configured Guides and Reference navigation. No separate custom React/Vue component library is configured in the project at this time.

## Getting started

### Prerequisites

- [Node.js](https://nodejs.org/) (a current supported LTS release is recommended)
- npm

### Install dependencies

```sh
npm install
```

### Start the local development server

```sh
npm run dev
```

Open the local URL printed by Astro, typically `http://localhost:4321`.

### Build and preview

```sh
npm run build
npm run preview
```

The production site is generated in `dist/`.

## Available commands

| Command | Description |
| --- | --- |
| `npm run dev` | Start the local development server. |
| `npm run start` | Alias for `npm run dev`. |
| `npm run build` | Build the production site. |
| `npm run preview` | Preview the production build locally. |
| `npm run astro -- <command>` | Run an Astro CLI command. |

## Adding documentation

Create `.md` or `.mdx` pages under `src/content/docs/`. Starlight turns these files into documentation routes. For example:

```text
src/content/docs/
├── index.mdx
├── guides/
│   └── getting-started.md
└── reference/
    └── configuration.md
```

Update the sidebar in `astro.config.mjs` when you add or reorganize navigation. Put images imported by documentation in `src/assets/`; place files that should be served directly in `public/`.

## Learn more

- [Astro documentation](https://docs.astro.build/)
- [Starlight documentation](https://starlight.astro.build/)
- [Markdown guide](https://www.markdownguide.org/)

## License

No license is currently specified in this repository. Add a `LICENSE` file if you want to make reuse terms explicit.
