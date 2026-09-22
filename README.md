<div align="center">

# Sephiro

### A considered set of UI primitives for desktop apps.

Composable, themeable components for React and Preact. Bring your own app shell; Sephiro brings the details that make it feel finished.

[![npm version](https://img.shields.io/npm/v/%40zovaris%2Fsephiro?logo=npm&logoColor=white)](https://www.npmjs.com/package/@zovaris/sephiro)
[![monthly downloads](https://img.shields.io/npm/dm/%40zovaris%2Fsephiro?label=downloads%2Fmonth)](https://www.npmjs.com/package/@zovaris/sephiro)
[![license](https://img.shields.io/npm/l/%40zovaris%2Fsephiro)](https://www.npmjs.com/package/@zovaris/sephiro?activeTab=license)

![React](https://img.shields.io/badge/React-18%2B-61DAFB?logo=react&logoColor=20232A)
![Preact](https://img.shields.io/badge/Preact-compatible-673AB8?logo=preact&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-typed-3178C6?logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-v4-06B6D4?logo=tailwindcss&logoColor=white)

[Website](https://sephiro.justcallmebryan.com) · [npm package](https://www.npmjs.com/package/@zovaris/sephiro) · [Zovaris](https://github.com/Zovaris)

</div>

---

Sephiro is a UI toolkit for product interfaces, especially desktop apps built with Tauri or Electron. It gives you reusable controls and patterns without imposing a page framework, a global reset, or a single visual identity.

## Why Sephiro

- **Fits into your app.** Component styles are namespaced and the stylesheet does not apply a global reset.
- **Theme at the boundary.** Apply a preset to an ancestor with `data-sephiro-theme`; separate areas of an app can use different themes.
- **Choose your CSS contract.** Import the complete stylesheet, or import theme tokens and component rules separately.
- **Use your framework.** Build with React 18+ or use Preact through its React compatibility layer.
- **Keep your own identity.** Semantic `--sph-*` tokens make it possible to tune the toolkit without rewriting each component.

## Install

```bash
# Bun
bun add @zovaris/sephiro

# npm
npm install @zovaris/sephiro
```

## Quick start

Import the components you need and the complete compiled stylesheet:

```tsx
import { Button } from "@zovaris/sephiro";
import "@zovaris/sephiro/styles.css";

export function CreateProjectButton() {
  return (
    <div data-sephiro-theme="light">
      <Button variant="primary">Create project</Button>
    </div>
  );
}
```

The stylesheet is already compiled. You do not need to add Sephiro to Tailwind's source scan.

### Tailwind CSS 4

Import the theme tokens and component styles separately when you want to control the CSS boundary yourself:

```tsx
import "@zovaris/sephiro/themes.css";
import "@zovaris/sephiro/components.css";
```

Use only `components.css` if your app provides its own `--sph-*` tokens.

## Themes

Set `data-sephiro-theme` on any ancestor to scope a preset to that part of the UI:

```tsx
<main data-sephiro-theme="asterism">
  <Button variant="primary">Open workspace</Button>
</main>
```

Presets: `default`, `dark`, `light`, `asterism`, `fizza`, and `pulso`. Multiple presets can coexist in the same app.

## What's inside

Buttons and form controls, menus and command surfaces, dialogs and popovers, tabs and toolbars, tables, notifications, layout primitives, and more. Import components directly from `@zovaris/sephiro` and let TypeScript guide their props.

## License

The current Sephiro codebase and future npm releases use the [PolyForm Perimeter License 1.0.0](./LICENSE), a source-available license that restricts using Sephiro to provide a competing product. It permits using the package in products that do not compete with Sephiro. See [NOTICE](./NOTICE) for the required copyright notice. Previously published npm versions remain under the license included with each release.

## Links

- [Website](https://sephiro.justcallmebryan.com)
- [Package on npm](https://www.npmjs.com/package/@zovaris/sephiro)
- [Package contents and versions](https://unpkg.com/browse/@zovaris/sephiro/)
- [Zovaris on GitHub](https://github.com/Zovaris)

This repository is the public product guide. The distributable package is published on npm; its package page lists the files and license.
