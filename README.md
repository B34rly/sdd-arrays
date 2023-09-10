# for miss
hi
this is clearly not vb.net
i also could not find an easy way to compile to windows while on linux. i want to sleep so i'm not doing the hard way

uh all the code is in the .svelte files in ./src/routes
the javascript is simple and svelte bindings are very simple and easy to use/understand! so you should have no problem reading through

oh and to build/run you will need npm, rust, and tauri
npm install (in the directory)
install rust and tauri (https://tauri.app/v1/guides/getting-started/prerequisites)
cargo tauri dev (or build! dev'll just be easier. about 5 minutes on the first build)

# create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.
