<template>
  <header class="position-relative">
    <div class="custom-container px-3">
      <div class="row justify-content-between align-items-center h-100">
        <div class="col-2">
          <img
            :src="getImagePath(`../assets/imgs/${imgData.imgPath}`)"
            :alt="`${imgData.imgAlt}`"
          />
        </div>
        <div class="col-6">
          <NavbarComponent />
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import NavbarComponent from "./NavbarComponent.vue";

export default {
  name: "HeaderComponent",
  components: {
    NavbarComponent,
  },
  data() {
    return {
      imgData: {
        imgPath: "dc-logo.png",
        imgAlt: "DC Logo",
      },
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
header {
  z-index: 999;
}
</style>
