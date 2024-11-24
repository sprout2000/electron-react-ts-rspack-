# electron-react-ts-rspack

<img src="https://user-images.githubusercontent.com/52094761/226554131-16510c26-7faf-4bf0-b271-a00abf66d9b5.svg#gh-light-mode-only">
<img src="https://user-images.githubusercontent.com/52094761/226554362-4a04fbd0-6918-47cd-abee-83c6c82a6877.svg#gh-dark-mode-only">

An [Electron](https://www.electronjs.org/) boilerplate with hot reloading for [React](https://reactjs.org/) and [TypeScript](https://www.typescriptlang.org/).

## :green_book: Usage

```sh
$ git clone https://github.com/sprout2000/electron-react-ts-rspack.git
$ cd electron-react-ts-rspack
$ npm install

# on development
$ npm run dev

# on production
$ npm run build
```

_NOTE: You will need to have [Node.js](https://nodejs.org/) and [Git](https://git-scm.com/) installed._

## :thumbsup: Features

- Supports hot reloading in both the main and renderer processes.
- No complicated pre-made settings.

The template provided by this scaffold is _NOT_ an all-in-one. It provides only the necessary and sufficient settings so that you can customize it as you like. In other words, it has no _"eject"_.

## :camera_flash: Screen shots

### Hot reload in renderer process

<img width="800" src="https://user-images.githubusercontent.com/52094761/235551732-a69ba9d5-db95-4101-9b79-e2741f8050dc.gif" />

### Hot reload in main process

<img width="800" src="https://user-images.githubusercontent.com/52094761/235551746-490c7b46-8d34-45a8-bd96-9afb0d37cb61.gif" />

## :package: How to package your app to publish?

It is recommended to use [electron-builder](https://www.electron.build/).

```sh
npm install --save-dev electron-builder
```

Here's a sample script `builder.ts` for electron-builder:

```typescript
import { build } from "electron-builder";

build({
  config: {
    appId: "com.example.MyApp",
    productName: "My App",
    artifactName: "${productName}-${version}-${platform}-${arch}.${ext}",
    files: ["dist/**/*"],
    directories: {
      output: "release",
    },
  },
});
```

And then run the script above...

```sh
npx ts-node ./builder.ts
```

See [Common Configuration](https://www.electron.build/configuration) for more details.
