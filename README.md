# create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm init svelte@next

# create a new project in my-app
npm init svelte@next my-app
```

> Note: the `@next` is temporary

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


To add sass to your already existing svelte + tailwind project to help customise your website

First of all create a folder in the src named css and create these files respectively
- main.scss
- _variables.scss
- _mixins.scss

add the tailwind.css inside the css folder and add the tailwind classes
@tailwind base;
@tailwind components;
@tailwind utilities;
 
dont forget to add a watch script in your package.json
"watch-sass": "sass -w src/css/main.scss src/css/main.css"

In your tailwind config file dont forget to add the content and also to purge your site
purge: ['./src/**/*.{html,js,svelte,ts}'],
content: ['src/**/*.{html,css,js,jsx,ts,tsx,svelte}'],

In your layout.svelte import the tailwind and the complied main.css file 

and boom you can start writng your custom styles in the main.scss file also dont forget to import your variables and your mixins file into the main.scss
