<template>
  <div>
    <AppLinks />
    <Nuxt />
  </div>
</template>

<script>
export default {
  head: {
    title: "Nuxt proovileht",
    meta: [
      {
        hid: "Siia mingi HID kirjeldus",
        name: "Siia nime kirjeldis",
        content: "Siia sisu kirjeldus",
      },
    ],
    bodyAttrs: {
      class:
        "home-page home page page-id-4 page-template page-template-template-homepage page-template-template-homepage-php",
    },
  },
};
</script>
