# svelte-stacks-icons

[![NPM][npm]][npm-url]

> [Stack Overflow Stacks SVG icons](https://github.com/StackExchange/Stacks-Icons) as Svelte components.

<!-- REPO_URL -->

<!-- Try it in the [Svelte REPL](). -->

---

<!-- TOC -->

## Installation

**Yarn**

```bash
yarn add -D svelte-stacks-icons
```

**NPM**

```bash
npm i -D svelte-stacks-icons
```

## Usage

### Basic

```svelte
<script>
  import { Alert, Calendar, Eye } from "svelte-stacks-icons";
</script>

<Alert />
<Calendar />
<Eye />
```

Refer to [ICON_INDEX.md](ICON_INDEX.md) for a list of supported icons.

### Direct import

Use the direct import for faster compiling during development.

**Note:** even if using base imports, unused imports are still tree shakeable by application bundlers like Rollup or webpack.

```html
<script>
  import Add from "svelte-stacks-icons/lib/Add.svelte";
</script>
```

## Rendering icons using `svelte:component`

```svelte
<script>
  import * as icons from "svelte-stacks-icons";
</script>

{#each Object.entries(icons) as [icon, component]}
  <div>
    <svelte:component this={component} />
    {icon}
  </div>
{/each}
```

## TypeScript

Svelte version 3.31 or greater is required to use this library with TypeScript.

## [Changelog](CHANGELOG.md)

## License

[MIT](LICENSE)

[npm]: https://img.shields.io/npm/v/svelte-stacks-icons.svg?color=%23f48225&style=for-the-badge
[npm-url]: https://npmjs.com/package/svelte-stacks-icons
