# demo-shared-webc-components

This is a barebones repo that provides one demo [WebC](https://github.com/11ty/webc) component for use by other projects.

## Demo

[See the live demo](https://ashur-shared-webc-demo.netlify.app) of an external site that uses this project's component, installed via NPM.

## Usage

You probably don't want to use this for real, but if you did this is what you'd do.

First, install this repo as a package:

```shell
npm install ashur/demo-shared-webc-components#semver:^v0.1.0
```

> **Note** — It feels a little silly to publish an entire package to NPM just for a quick demo, so this is the [syntax](https://docs.npmjs.com/cli/v8/commands/npm-install) for installing from a GitHub repo.
>
> If it were published to NPM, the install command might look like the more traditional:
> ```shell
> npm install @aaashur/demo-shared-webc-components
> ```

Next, drop this snippet into your WebC markup:

```html
<confetti-button
    webc:import="npm:@aaashur/demo-shared-webc-components">
</confetti-button>
```

> **Note** — Even though we installed from GitHub, the package is installed at `./node_modules/@aaashur/demo-shared-webc-components` (because that's what I called it in [`package.json`](/package.json#L2)) so that's how it should be referenced by the WebC import.

If you want to be fancy and set a custom button label, use the `text` prop:

```html
<confetti-button
    text="It’s Confetti Time"
    webc:import="npm:@aaashur/demo-shared-webc-components">
</confetti-button>
```
