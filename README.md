# vue3-repos.github.io

Source for the demonstration website of the [vue3-repos](https://github.com/vue3-repos) GitHub organisation, published at **https://vue3-repos.github.io/**.

The site shows the libraries in the organisation working inside a real Vue 3 application. It currently demonstrates:

- **[vue3-katex](https://github.com/vue3-repos/vue3-katex)**: math and chemistry rendering with KaTeX. The examples cover the `v-katex` directive (`display`, `inline` and `auto` modes), the `KatexElement` component, and chemical equations through the `mhchem` extension.

More libraries from the organisation will be added over time.

## Development

The site is built with [Vite](https://vite.dev/).

```bash
yarn install
yarn dev      # start a local development server
yarn build    # build the site into dist/
yarn preview  # serve the built site locally
```

Each demonstration lives in its own component under `src/components/`. Plugins are registered in `src/main.js`.

## Deployment

Every push to `main` triggers the [deploy workflow](.github/workflows/deploy-website.yml). It builds the site and force-pushes the contents of `dist/` to the `website` branch, and GitHub Pages serves the site from that branch.

## License

Licensed under the [Apache License 2.0](LICENSE).
