<template>
  <div class="custom-container position-relative">
    <div class="row align-items-center h-100">
      <div class="col-5 py-4-5 d-flex flex-column flex-wrap h-100">
        <ul v-for="(list, index) in navigationLists">
          <h4 class="text-white">{{ list.title }}</h4>
          <li v-for="listTxt in list.listEls">
            <a href="#">{{ listTxt }}</a>
          </li>
        </ul>
      </div>
    </div>
    <img src="../assets/imgs/dc-logo-bg.png" alt="" class="dc-bg-logo" />
  </div>
</template>

<script>
export default {
  name: "NavigationComponent",
  data() {
    return {
      navigationLists: [
        {
          title: "dc comics",
          listEls: [
            "characters",
            "comics",
            "movies",
            "tv",
            "games",
            "videos",
            "news",
          ],
        },

        {
          title: "shop",
          listEls: ["shop DC", "shop DC collectibles"],
        },

        {
          title: "dc",
          listEls: [
            "terms of use",
            "privacy policy (new)",
            "ad choices",
            "advertising",
            "jobs",
            "subscriptions",
            "talent workshop",
            "CPSC certificates",
            "ratings",
            "shop help",
            "contact us",
          ],
        },

        {
          title: "sites",
          listEls: [
            "DC",
            "MAD magazine",
            "DC kids",
            "DC universe",
            "DC power visa",
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.custom-container {
  height: 24rem;
}

.py-4-5 {
  padding: 1.95rem 0;
}

a {
  color: #959595;
  text-decoration: none;
}
.dc-bg-logo {
  z-index: 1;
  position: absolute;
  top: -7rem;
  right: 5rem;
  width: 37rem;
}
</style>
