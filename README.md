# Mobile Jazz Prettier Config

Shared Prettier config used in Mobile Jazz projects.

## Usage

Usage is based on [Sharing configurations](https://prettier.io/docs/en/configuration.html#sharing-configurations) from the Prettier docs.

1. Remove existing `.prettierrc` file, if present.
1. Install the config. Note that you'll also need to install Prettier.

    ```sh
    npm install -D prettier # if it's not already installed
    npm install -D @mobilejazz/prettier-config
    ```

1. Add the following to `package.json`:

    ```json
    "prettier": "@mobilejazz/prettier-config",
    ```

### Applying Overrides

For legacy projects it's OK to override the `tabWidth` configuration; **no other option should be overriden**.

1. If present, remove existing `.prettierrc` file and/or `prettier` entry in `package.json`.
1. Create a `.prettierrc.js` file, with the following content:

    ```js
    module.exports = {
      ...require("@mobilejazz/prettier-config"),
      tabWidth: 4,
    };
    ```

For further details refer to the [Prettier documentation](https://prettier.io/docs/en/configuration.html#sharing-configurations).
