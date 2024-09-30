# Importmap for `@butility` Packages

This repository provides an **import map JSON** file that simplifies importing modules from the `@butility` package family directly from `node_modules` without requiring the exact directory names.

## Overview

In typical JavaScript, in browser, when importing modules from `node_modules`, you often need to know the precise directory structure. This can be hard, especially when working with scoped packages like `@butility`. 

The **import map** defined in this repository eliminates the need for perfect directory names, allowing you to easily map module names to their corresponding paths in `node_modules` for @butility pkgs.

## Key Features

- Simplifies module imports for `@butility` packages for browsers.
- Eliminates the need to reference exact directory structures within `node_modules`.
- Provides a cleaner and more intuitive way to import modules.

## Usage

1. Clone this repository or copy the provided `importmap.json` file into your project.
2. Add a reference to the `importmap.json` in your project configuration (e.g., for browsers that support import maps inside script tag or using a bundler that supports import maps).
3. Now, when you import `@butility` modules, they will be correctly resolved from `node_modules` without worrying about exact directory names.

## Example

### Before Import Map
```js
import { body } from './node_modules/@butility/dom/html.js';
```

### After Import Map
```js
import { body } from '@butility/html';
```

## Setup

To use this import map in your project:

1. Ensure that your project supports import maps (e.g., using a compatible bundler or runtime).
2. Add the `importmap.json` file to your project.
3. Reference the import map in your application entry point or configuration.

```json
{
  "imports": {
    "@butility/dom": "./node_modules/@butility/dom/dom.js"
  }
}
```

Now, the specified modules will be resolved from the correct paths within `node_modules` without the need for perfect directory names.

## License

This repository is open source and available under the [MIT License](LICENSE.md).
