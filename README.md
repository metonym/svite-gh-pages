# svite-minimal

> [Minimal Svite set-up](https://github.com/dominikg/svite/tree/master/examples/minimal) made deployable to [GitHub pages](https://metonym.github.io/svite-minimal/).

Customize the base directory and assets directory.

- `base` should be either "" (relative path) or the public path of your GH repo (i.e. "/svite-minimal/")
- `assetsDir` should not begin with an underscore (GitHub pages [ignores folders beginning with "\_"](https://github.blog/2009-12-29-bypassing-jekyll-on-github-pages/))

```diff
"scripts": {
-  "build": "svite build",
+  "build": "svite build --base= --assetsDir=assets",
}
```

## Deploying to GitHub Pages

First, build the app by running `yarn build`.

Then, run `yarn deploy`.

## Additional notes

- Incorporates MDsveX
- Replaces "process.env.VERSION" in script code with the `version` from `package.json` (useful for component libraries)
