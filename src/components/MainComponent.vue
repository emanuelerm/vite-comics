<template>
  <main>
    <section id="content">
      <div class="custom-container d-flex align-items-center h-100">
        <div class="row align-items-center">
          <div class="col">
            <h3 class="text-white mb-0">{{ contentText }}</h3>
          </div>
        </div>
      </div>
    </section>

    <section id="benefits">
      <BenefitsComponent />
    </section>

    <section id="navigation">
      <NavigationComponent />
    </section>
  </main>
</template>

<script>
import BenefitsComponent from "./BenefitsComponent.vue";
import NavigationComponent from "./NavigationComponent.vue";

export default {
  name: "MainComponent",
  components: {
    BenefitsComponent,
    NavigationComponent,
  },
  data() {
    return {
      contentText: "----> Content goes here <----",
    };
  },
};
</script>

<style lang="scss" scoped>
main {
  height: 43rem;
  z-index: 999;
  #content {
    height: 8rem;
    background-color: #1c1c1c;
  }
  #benefits {
    height: 11rem;
    background-color: #0c7cec;
    position: relative;
    z-index: 999;
  }
  #navigation {
    height: 24rem;
    background-image: url(../assets/imgs/footer-bg.jpg);
    background-position: top;
    background-size: cover;
  }
}
</style>
