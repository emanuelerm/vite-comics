<template>
  <div class="custom-container h-100">
    <div class="row row-cols-5 align-items-center h-100">
      <div
        v-for="itemEl in benefitsCardEls"
        class="col d-flex align-items-center px-5"
      >
        <img
          :src="getImagePath(`../assets/imgs/${itemEl.imgPath}`)"
          alt=""
          :class="itemEl.cardText === 'dc power visa' ? 'un-width' : ''"
        />
        <p class="text-white ps-3 m-0">
          {{ itemEl.cardText }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BenefitsComponent",
  data() {
    return {
      benefitsCardEls: [
        {
          imgPath: "buy-comics-digital-comics.png",
          imgAlt: "digital comics",
          cardText: "digital comics",
        },

        {
          imgPath: "buy-comics-merchandise.png",
          imgAlt: "dc merchandise",
          cardText: "dc merchandise",
        },

        {
          imgPath: "buy-comics-subscriptions.png",
          imgAlt: "subscription",
          cardText: "subscription",
        },

        {
          imgPath: "buy-comics-shop-locator.png",
          imgAlt: "comic shop locator",
          cardText: "comic shop locator",
        },

        {
          imgPath: "buy-dc-power-visa.svg",
          imgAlt: "dc power visa",
          cardText: "dc power visa",
        },
      ],
    };
  },
  methods: {
    getImagePath: function (path) {
      return new URL(path, import.meta.url).href;
    },
  },
};
</script>

<style lang="scss" scoped>
img {
  height: 5rem;
}

.un-width {
  width: 5rem;
}
</style>
