# Rollup plugin less tilde importer

> A rollup plugin providing ~ (tilde) prefix as a way to tell less compiler that it should resolve path using a configured array of module directories.

## Install

```sh
yarn add -D @ovh-ux/rollup-plugin-less-tilde-importer
```

## Usage

```js
import less from 'rollup-plugin-less';
import lessTildeImporter from '@ovh-ux/rollup-plugin-less-tilde-importer';
import path from 'path';

export default {
  input: './src/index.js',
  output: {
    dir: './dist',
    format: 'cjs',
    sourcemap: true,
  },
  plugins: [
    lessTildeImporter({
      paths: [
        path.resolve(__dirname, './node_modules'),
        path.resolve(__dirname, '../../node_modules'),
      ],
    }),
    less(),
  ],
};
```

## Contributing

Always feel free to help out! Whether it's [filing bugs and feature requests](https://github.com/ovh-ux/rollup-plugin-less-tilde-importer/issues/new) or working on some of the [open issues](https://github.com/ovh-ux/rollup-plugin-less-tilde-importer/issues), our [contributing guide](CONTRIBUTING.md) will help get you started.

## License

[BSD-3-Clause](LICENSE) © OVH SAS
