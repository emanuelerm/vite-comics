<template>
  <ul class="d-flex justify-content-between list-unstyled">
    <li v-for="navItem in navbarEls" class="text-uppercase">
      <a :href="`${navItem.hrefLink}`">{{ navItem.textLink }}</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "NavbarComponent",
  data() {
    return {
      navbarEls: [
        {
          textLink: "characters",
          hrefLink: "#",
          active: false,
        },

        {
          textLink: "comics",
          hrefLink: "#",
          active: false,
        },
        {
          textLink: "movies",
          hrefLink: "#",
          active: false,
        },
        {
          textLink: "tv",
          hrefLink: "#",
          active: false,
        },
        {
          textLink: "games",
          hrefLink: "#",
          active: false,
        },
        {
          textLink: "collectibles",
          hrefLink: "#",
          active: false,
        },
        {
          textLink: "videos",
          hrefLink: "#",
          active: false,
        },
        {
          textLink: "fans",
          hrefLink: "#",
          active: false,
        },
        {
          textLink: "news",
          hrefLink: "#",
          active: false,
        },
        {
          textLink: "shop",
          hrefLink: "#",
          active: false,
        },
      ],
    };
  },
};
</script>

<style class="scss" scoped>
a {
  font-size: 1.1rem;
  text-decoration: none;
}
</style>
