# @kobalte/tailwindcss

A TailwindCSS plugin for styling Kobalte Elements with `data-*` attributes by using modifiers like `ui-expanded:*`.

## Installation

```bash
npm install -D @kobalte/tailwindcss
# or
yarn add -D @kobalte/tailwindcss
# or
pnpm add -D @kobalte/tailwindcss
```

## Usage

Add the plugin to your `tailwind.config.js`:

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [],
  theme: {
    extend: {},
  },
  plugins: [
    // default prefix is "ui"
    require("@kobalte/tailwindcss"),

    // or with a custom prefix:
    require("@kobalte/tailwindcss")({ prefix: "kb" }),
  ],
};
```

Style your component:

```tsx
import { Popover } from "@kobalte/elements";

export const MyPopover = () => (
  <Popover>
    <Popover.Trigger class="ui-disabled:bg-slate-100">Open</Popover.Trigger>
    <Popover.Content class="ui-expanded:shadow-md">...</Popover.Content>
  </Popover>
);
```

You can use the following modifiers:

| Modifier           | Inverse modifier       |
| :----------------- | :--------------------- |
| `ui-valid`         | `ui-not-valid`         |
| `ui-invalid`       | `ui-not-invalid`       |
| `ui-required`      | `ui-not-required`      |
| `ui-disabled`      | `ui-not-disabled`      |
| `ui-readonly`      | `ui-not-readonly`      |
| `ui-checked`       | `ui-not-checked`       |
| `ui-indeterminate` | `ui-not-indeterminate` |
| `ui-selected`      | `ui-not-selected`      |
| `ui-pressed`       | `ui-not-pressed`       |
| `ui-expanded`      | `ui-not-expanded`      |
| `ui-hover`         | `ui-not-hover`         |
| `ui-focus`         | `ui-not-focus`         |
| `ui-focus-visible` | `ui-not-focus-visible` |
| `ui-active`        | `ui-not-active`        |

## Documentation

For full documentation, visit [kobalte.dev](https://kobalte.dev/docs/overview/styling#using-the-tailwindcss-plugin).

## Acknowledgment

This plugin is an adaptation of [@headlessui/tailwindcss](https://github.com/tailwindlabs/headlessui), MIT Licensed, Copyright (c) 2020 Tailwind Labs.

## Changelog

All notable changes are described in the [CHANGELOG.md](./CHANGELOG.md) file.