<template>
  <ul class="d-flex justify-content-between list-unstyled mb-0">
    <li v-for="navItem in navbarEls" class="text-uppercase mx-2">
      <a
        :href="`${navItem.hrefLink}`"
        class="position-relative"
        :class="navItem.active ? 'active' : ''"
        >{{ navItem.textLink }}</a
      >
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
          active: true,
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

<style lang="scss" scoped>
a {
  font-size: 1.2rem;
  color: black;
  text-decoration: none;

  &:hover {
    color: #0c7cec;
  }

  &::after {
    opacity: 0;
    content: "";
    position: absolute;
    bottom: -54px;
    left: 0;
    width: 100%;
    height: 5px;
    background-color: #0c7cec;
    transform: scaleY(0);
    transition: all 300ms ease-in;
  }

  &:hover::after {
    opacity: 1;
    transform: scaleY(1);
  }
}

.active {
  color: #0c7cec;

  &::after {
    content: "";
    position: absolute;
    bottom: -54px;
    left: 0;
    width: 100%;
    height: 5px;
    background-color: #0c7cec;
    opacity: 1 !important;
    transform: scaleY(1);
  }
}
</style>
