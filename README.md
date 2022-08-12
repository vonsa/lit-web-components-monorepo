## Info

This is vonsa's web component UI kit

## Installation

```
yarn install
lerna bootstrap
```

## Developing

You can test elements inside of an existing project, with live reloading.

In this repo, run:
```yarn link```

In your existing project:

Add `@vonsa/web-components-monorepo` as a dependency, with version number `*`.

run:
```yarn link @vonsa/web-components-monorepo```

Now, in the web components monorepo, run:
```lerna run build:watch```

Now, whenever you make a change in the web components monorepo, your existing project will be reloaded with the latest changes.

## Project structure

This project is setup using a monorepo structure.
Each Lit element is added as a separate package and inherits from the main monorepo configuration. This allows each element to be published as a separate package, this also means they can be used without a compiler.
There is also a collection package which bundles all Lit elements together. When you include this package in your project, you can import what you need and tree shaking will ensure only imported elements are included in the bundle.