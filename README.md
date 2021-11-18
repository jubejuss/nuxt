# nuxt-one

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out the [documentation](https://nuxtjs.org).

## Special Directories

You can create the following extra directories, some of which have special behaviors. Only `pages` is required; you can delete them if you don't want to use their functionality.

### `assets`

The assets directory contains your uncompiled assets such as Stylus or Sass files, images, or fonts.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/assets).

### `components`

The components directory contains your Vue.js components. Components make up the different parts of your page and can be reused and imported into your pages, layouts and even other components.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/components).

### `layouts`

Layouts are a great help when you want to change the look and feel of your Nuxt app, whether you want to include a sidebar or have distinct layouts for mobile and desktop.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/layouts).

### `pages`

This directory contains your application views and routes. Nuxt will read all the `*.vue` files inside this directory and setup Vue Router automatically.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/get-started/routing).

### `plugins`

The plugins directory contains JavaScript plugins that you want to run before instantiating the root Vue.js Application. This is the place to add Vue plugins and to inject functions or constants. Every time you need to use `Vue.use()`, you should create a file in `plugins/` and add its path to plugins in `nuxt.config.js`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/plugins).

### `static`

This directory contains your static files. Each file inside this directory is mapped to `/`.

Example: `/static/robots.txt` is mapped as `/robots.txt`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/static).

### `store`

This directory contains your Vuex store files. Creating a file in this directory automatically activates Vuex.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/store).

## Isetehtud osa

Nuxti põhimõte on see, et on lehed `pages` folderis ja komponendid `components` folderis. Komponentide all defineerid erinevad komponendid, nt `NavBar.vue`, mille sees võib ka olla komponent, nt `AppLinks.vue`. nimed pole tähtsad, aga need siis impordid oma lehele, nt `index.vue`sse

[Üks võimalik juhend](https://www.codementor.io/@cejowisz/navigation-drawer-tutorial-with-nuxt-rrax23tmw)  
Käesolev leht on tehtud Nuxt+Tailwindiga [Juhend](https://tailwindcss.nuxtjs.org/)

Nuxti globaalne päis pannakse paika `nuxt.config.js` failis

### Tailwind CSS

Tailwindi confimiseks võib teha juurikasse `tailwind.config.js` faili.  
Tailwind on vaikimisi vasakule joondumisega, seega tsentreerimiseks peaks kasutama `mx-auto` klassi või siis `tailwind.config.js`-i lisama:

```javascript
module.exports = {
  theme: {
    container: {
      center: true,
    },
  },
};
```

Siin on tehtud nii, et kõigepealt `npx tailwindcss init`

**_ Default Layout _**
Kui tahta mingeid asju, mis mõjuks kõikjale, tuleks teha `default.vue` ja pista see `layouts` foldersse, mis tuleb samuti luua. Tolle sees peab olema kindlasti, vähemat alul:

```nuxt
<template>
  <Nuxt />
</template>
```

Kui see tehtud, saab kõikide lehtede ühiseid asju, nt body css või head meta, pista sinna.

[Täpsem juhend](https://nuxtjs.org/docs/concepts/views/#html-head)

**_ Default layouti sisse minev _**  
Näidiseid, kuidas kirjutada default.vue-sse metainfot vms, vaata [**_ siit _**](https://nuxtjs.org/docs/features/meta-tags-seo/)

body jms kohta leiad juhendi [**_ siit _**](https://vue-meta.nuxtjs.org/api/#bodyattrs)

**_ Oma Css-i lisamine ja page transitionid _**
https://blog.logrocket.com/css-transitions-in-nuxt-js-an-overview/
https://dev.to/debs_obrien/page-and-layout-transitions-in-nuxt-js-33f

Transitionid
https://debbie.codes/blog/nuxt-page-and-layout-transitions/
