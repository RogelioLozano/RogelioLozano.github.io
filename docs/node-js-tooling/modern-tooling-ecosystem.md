---
sidebar_position: 1
---

# Modern Tooling

This will keep a record of the relations and interactions among the tools of a constantly evolving modern tooling ecosystem that I'll use.

## My current Stack options
 + (TailwindCSS + daisyUI) or Boostrap: For...
 
 + Skeleton optional: For...
 
 + PostCSS + SCSS: For...
 
 + SvelteKit or NextJS: For...

 + Vite: For...


## client-side tools are broadly categorized in three.

### Tools used during code development
Code formatters ([Prettier](https://prettier.io/) has plugins for other languages besides javascript), Linting tools ([ESLint](https://eslint.org/) for javascript for example), Source code control (git), and Bundlers/packagers which are tools that get code ready for production environments, for example by "tree-shaking" to make sure only necessary the parts of code that are actually being used are put into the final production code, or "minifying" to remove all whitespaces as making the code as small as possible before being uploaded to a server (Parcel, Webpack, [Vite](https://vitejs.dev/)). Vite, for examples uses rollup.js as the module boundler.

### Transformation tools
 Transform the code in some way. Usually turns an intermediate language into javascript (or css or something else, depeding) that a browser can understand. Here are tools like **Typescript**, **Babel** and **PostCSS**.

 Babel and PostCSS allow to use the latest or required version of javascript and CSS respectively while the resulting transformed code is more browser-compatible (code that is supported by older browsers).

Typescript, React, Svelte are all extensions to the javascript language that provide extended functionality via custom syntax on top of vanilla JS. Sass/SCSS does the same but for CSS.

### Post-development
 Testing and deployment; tools that you use after written code. Testing tools, CICD, deployment tools like [Netlify](https://www.netlify.com/) and [Vercel](https://vercel.com/).

