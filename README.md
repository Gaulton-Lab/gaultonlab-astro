# Gaulton Lab Website

Source for [gaultonlab.org](https://www.gaultonlab.org/), the website of the Gaulton Lab at UC San Diego. Built with [Astro](https://astro.build/) using a customized [Devosfera](https://github.com/0xdres/devosfera) theme.

## Local development

Requires Node.js 20+.

```bash
npm install
npm run dev
# http://localhost:4321
```

To test search locally, build first (the Pagefind index is only generated during production builds):

```bash
npm run build
npm run preview
```

## Updating content

### People

Edit `src/pages/people.astro`. Each person is defined inline with their name, role, links, and photo. Photos go in `src/assets/images/people/`.

### Publications

Edit `src/pages/publications.astro`. Papers are organized by year in the `publications` array. Each entry has `title`, `authors`, `journal`, and `doi`.

### Resources

Edit `src/pages/resources.astro`. Research data pages (islet genomics, T1D, etc.) are individual pages under `src/pages/pages/`.

### Photos

Add images to `src/assets/images/photos/` and update the gallery in `src/pages/photos.astro`.

## Configuration

Site-wide settings (title, description, feature toggles) are in `src/config.ts`. Social links are in `src/constants.ts`.

## Deployment

Pushes to `main` automatically deploy to GitHub Pages via the workflow in `.github/workflows/`.

## License

MIT. Based on [Devosfera](https://github.com/0xdres/devosfera) by [0xdres](https://github.com/0xdres), which is based on [AstroPaper](https://github.com/satnaing/astro-paper) by [Sat Naing](https://satnaing.dev).
