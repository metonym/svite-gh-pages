# svite-gh-pages

> [Minimal Svite set-up](https://github.com/dominikg/svite/tree/master/examples/minimal) made deployable to [GitHub pages](https://metonym.github.io/svite-gh-pages/).

Customize the base directory and assets directory.

- `base` should be either "" (relative path) or the public path of your repo (i.e. "/svite-gh-pages/")
- `assetsDir` should not begin with an underscore (GitHub Pages [ignores folders beginning with "\_"](https://github.blog/2009-12-29-bypassing-jekyll-on-github-pages/))

```diff
"scripts": {
-  "build": "svite build",
+  "build": "svite build --base= --assetsDir=assets",
}
```

## Quick start

Use [degit](https://github.com/Rich-Harris/degit) to quickly scaffold a new project:

```sh
npx degit metonym/svite-gh-pages my-app
cd my-app && yarn install
```

## Deploying to GitHub Pages

First, build the app by running `yarn build`.

Then, run `yarn deploy`.

## Additional notes

- Incorporates [MDsveX](https://github.com/pngwn/mdsvex)
- Uses svelte preprocess API too replace "process.env.NAME" and "process.env.VERSION" with the `name` and `version` from `package.json`. This is useful for documenting component libraries.
