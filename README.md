# Template to use TypeScript with k6, via [esbuild](https://esbuild.github.io/)

This is a template project based off of Grafana's own [k6 TypeScript template](https://github.com/grafana/k6-template-typescript).

The difference is that instead of using Webpack as a bundler, this template uses esbuild so you can iterate on your TypeScript-based tests at lightning speed.⚡

Example build:

```bash
$ pnpm build

> find ./src -name *.ts -exec esbuild '{}' --bundle --outbase=src --outdir=dist --external:k6 --format=esm \;


  dist/post-file-test.js  486b

⚡ Done in 1ms

  dist/get-200-status-test.js  379b

⚡ Done in 1ms

  dist/post-400-status-test.js  492b

⚡ Done in 1ms
```

## Scaffolding

You can quickly scaffold a new project using this template with `degit`

```bash
$ pnpm dlx degit nickcwilkins/k6-template-esbuild-typescript
```
