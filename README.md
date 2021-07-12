# Typescript Sass bit.dev initial workspace

If you use **typescript** and **sass** on your `bit.dev` component development, and **VS Code** is your editor of choice, this initial setup may be useful to you.

## The problem

If you try to use sass modules when developing your components in VS Code, you'll get errors saying the module can't be resolved.

## The solution

You can use this repo as your starting code, then just `bit install`, or use the following steps if you want to add the configuration to your current project:

1. `bit install sass`
2. `bit install typescript-plugin-css-modules`
3. `bit install typescript` locally, and configure it to use `typescript-plugin-css-modules` as a plugin in your `tsconfig.json` file:

```json
{
  "compilerOptions": {
    ...
    "plugins": [{ "name": "typescript-plugin-css-modules" }],
    ...
```

> NOTE: If you need an example of a `tsconfig.json` file, you can use this repository's file as reference

4. Have VS Code use your local workspace version of `TypeScript`, found in `node_modules`. You can [follow these instructions](https://code.visualstudio.com/docs/typescript/typescript-compiling#_using-the-workspace-version-of-typescript), or the easiest way is to create a `.vscode/settings.josn` file and add the following:

```json
{
  "typescript.tsdk": "node_modules/typescript/lib"
}
```

Star and share if you like this repo. Thanks!
