# export-typescript

## Functions

1. Automatically export typescript files when newly creating an index.ts file.
1. While in an `index.ts` file, run this extension ("Export Typescript: Write exports") to add `export * from ./<FILE_OR_FOLDER>` for each sibling file/folder in the current directory.
1. Explicitly export declarations like `export { Foo, Bar } from ./<FILE>` by setting `exportStar=false` in the config.

## Config

The default configuration exports all sibling `.ts` files and folders with a `index.ts` file.

```json
"export-typescript": {
  "exportStar": true,
  "includes": ["*.{ts,tsx}", "*/index.{ts,tsx}"],
  "excludes": ["*.{spec.ts,spec.tsx}"]
}
```

In order to export declarations and look for files in subdirectories recursively, put the following in your `.vscode/settings.json`:

```json
"export-typescript": {
  "exportStar": false,
  "includes": ["**/*.{ts,tsx}"],
  "excludes": ["**/*.{spec.ts,spec.tsx}"]
}
```

## Changelog

[CHANGELOG.md](https://github.com/mscolnick/export-typescript/blob/master/CHANGELOG.md)
