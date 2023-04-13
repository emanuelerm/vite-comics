<template>
  <header>
    <div class="custom-container">
      <div class="row justify-content-between">
        <div class="col-2">
          <img
            :src="getImagePath(`../assets/imgs/${imgData.imgPath}`)"
            :alt="`${imgData.imgAlt}`"
          />
        </div>
        <div class="col-6"></div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
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

<style class="scss" scoped></style>
