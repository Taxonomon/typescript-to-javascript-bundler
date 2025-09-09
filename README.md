# fivem-typescript-resource-bundler

Bundles FiveM TypeScript-based resources into JavaScript, based on [Jax Danger's ts-fivem-starterpack](https://github.com/Jax-Danger/ts-fivem-starterpack/blob/ts-react-fivem/fivem/build.js).

## Usage

At its core, this script takes all TypeScript code in a given directory and bundles it into a single JavaScript file using [esbuild](https://esbuild.github.io/).

### Config

To configure the inputs and outputs, simply add the relative or absolute paths to the `src/config.json`:

```json
[
  {
    "source": "../src/client", // takes all code in ../src/client
    "target": "../build/client.js", // and bundles it into ../build/client.js
    "enabled": true // whether to skip bundling this entry
  },
  {
    // ...
    // multiple entries are supported
    // ...
  }
]
```

### Run

Install all necessary dependencies:

```
npm i
```

And run the script:

```
npm run bundle
```

The script will then process all enabled config entries.

## License & Copyright

The original script was taken from [Jax Danger's ts-fivem-starterpack](https://github.com/Jax-Danger/ts-fivem-starterpack/blob/ts-react-fivem/fivem/build.js) with slight adjustments that fit to my personal needs when developing FiveM resources. So all credit to him for the original.

I do not own this script, nor do I have any saying about its licensing or copyright. Please refer to the original author's licensing and copyright information.
