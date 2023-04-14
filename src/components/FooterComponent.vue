<template>
  <footer class="position-relative">
    <div class="custom-container h-100">
      <div class="row justify-content-between align-items-center h-100">
        <div class="col-2">
          <button class="btn btn-outline-primary">sign-up now!</button>
        </div>
        <div class="col-4 d-flex justify-content-end">
          <p class="me-3 mb-0 fs-4">follow us</p>
          <a v-for="(img, index) in imgFooterData" :href="`${index}`"
            ><img
              :src="getImagePath(`../assets/imgs/${img.imgPath}`)"
              :alt="`${img.imgAlt}`"
          /></a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
  data() {
    return {
      imgFooterData: [
        {
          imgPath: "footer-facebook.png",
          imgAlt: "Facebook Logo",
        },

        {
          imgPath: "footer-periscope.png",
          imgAlt: "Periscope Logo",
        },

        {
          imgPath: "footer-pinterest.png",
          imgAlt: "Pinterest Logo",
        },

        {
          imgPath: "footer-twitter.png",
          imgAlt: "Twitter Logo",
        },

        {
          imgPath: "footer-youtube.png",
          imgAlt: "Youtube Logo",
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
footer {
  height: 7.05rem;
  background-color: #303030;
  z-index: 999;
  button {
    border-width: 3px;
    border-radius: 0;
    padding: 0.45rem 1rem;
    color: white;
    font-size: 1.3rem;
  }
  p {
    color: #0c7cec;
  }
  a {
    margin: 0 0.7rem;
  }
}
</style>
