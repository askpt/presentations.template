# Presentations Template

A ready-to-use template for creating beautiful, interactive presentations using [Slidev](https://sli.dev/). This template includes Vue components, pre-configured deployment settings, and a structured project layout to help you quickly build and deploy professional presentations. Learn more about Slidev at the [documentation](https://sli.dev/).

## Features

- ✨ **Slidev Integration** - Powerful slide deck framework with markdown support
- 🎨 **Multiple Themes** - Pre-configured with Seriph and Default themes
- 🧩 **Vue Components** - Reusable interactive components (e.g., Counter)
- 📁 **Organized Structure** - Clean separation of slides, components, and snippets
- 🚀 **Deploy Ready** - Pre-configured for Netlify and Vercel deployment
- 📝 **Slide Splitting** - Split presentations across multiple markdown files

## Quick Start

Install dependencies:

```bash
pnpm install
```

Start the development server:

```bash
pnpm dev
```

Visit <http://localhost:3030> to view your presentation.

Edit [slides.md](./slides.md) to customize your content. Changes will hot-reload automatically.

## Project Structure

```
.
├── slides.md              # Main presentation file
├── components/            # Vue components for slides
│   └── Counter.vue        # Example interactive component
├── pages/                 # Additional slide pages
│   └── imported-slides.md # Example of split slides
├── snippets/              # Code snippets and external files
│   └── external.ts        # Example TypeScript file
├── netlify.toml           # Netlify deployment configuration
└── vercel.json            # Vercel deployment configuration
```

## Building for Production

Build static files for deployment:

```bash
pnpm build
```

The built files will be output to the `dist/` directory.

## Deployment

### Netlify

This template includes a [netlify.toml](./netlify.toml) configuration. Simply connect your repository to Netlify, and it will automatically build and deploy your presentation.

### Vercel

This template includes a [vercel.json](./vercel.json) configuration. Connect your repository to Vercel for automatic deployments.

### Manual Deployment

After running `pnpm build`, deploy the `dist/` directory to any static hosting service.

## Customization

### Changing Themes

Edit the theme property in the frontmatter of [slides.md](./slides.md):

```yaml
---
theme: seriph # or 'default', or install other themes
---
```

### Adding Components

Place Vue components in the `components/` directory. They will be automatically available in your slides without imports.

### Splitting Slides

Use the `src` attribute to import slides from other files:

```markdown
---
src: ./pages/my-slides.md
---
```

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
