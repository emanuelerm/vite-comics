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
      <div class="custom-container"></div>
    </section>
  </main>
</template>

<script>
import BenefitsComponent from "./BenefitsComponent.vue";

export default {
  name: "MainComponent",
  components: {
    BenefitsComponent,
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
  #content {
    height: 8rem;
    background-color: #1c1c1c;
  }
  #benefits {
    height: 11rem;
    background-color: #0c7cec;
  }
  #navigation {
    height: 24rem;
    background-image: url(../assets/imgs/footer-bg.jpg);
    background-position: top;
    background-size: cover;
  }
}
</style>
