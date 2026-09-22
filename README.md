# Sephiro Toolkit

Composable, themeable UI primitives for React and Preact desktop apps.

Sephiro provides small components with semantic design tokens and scoped themes. It is designed to fit into Tauri, Electron, and web app shells without applying a global CSS reset.

## Install

```bash
bun add @zovaris/sephiro
```

Or with npm:

```bash
npm install @zovaris/sephiro
```

## Quick start

```tsx
import { Button, Field, Input } from "@zovaris/sephiro";
import "@zovaris/sephiro/styles.css";

export function Example() {
  return (
    <section data-sephiro-theme="light">
      <Field label="Project name">
        <Input placeholder="My project" />
      </Field>
      <Button variant="primary">Create project</Button>
    </section>
  );
}
```

The default stylesheet includes component styles and Sephiro theme tokens. For Tailwind CSS 4 projects, you can import these separately instead:

```tsx
import "@zovaris/sephiro/themes.css";
import "@zovaris/sephiro/components.css";
```

The package ships compiled CSS, so you do not need to add Sephiro to Tailwind's source scan.

## Themes

Set `data-sephiro-theme` on a component ancestor to scope a theme:

```html
<div data-sephiro-theme="asterism">
  <!-- Sephiro components use this theme -->
</div>
```

Available presets: `default`, `dark`, `light`, `asterism`, `fizza`, and `pulso`. Multiple presets can coexist on the same page.

## Components and API

The package includes buttons, form controls, dialogs, menus, popovers, tabs, toolbars, tables, notifications, and other reusable primitives. Component exports and their TypeScript props are available from `@zovaris/sephiro`.

## Links

- [Sephiro on npm](https://www.npmjs.com/package/@zovaris/sephiro)
- [Package files and version history](https://unpkg.com/browse/@zovaris/sephiro/)
- [Zovaris](https://github.com/Zovaris)

This repository contains product information and usage documentation. The distributable package is published on npm; see its npm page for the package license and files.
