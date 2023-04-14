<template>
  <main>
    <section id="jumbo">
      <img src="../assets/imgs/jumbotron.jpg" alt="" />
    </section>
    <section id="content">
      <button class="btn btn-lg btn-primary">current series</button>
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
  z-index: 999;
  #jumbo {
    height: 26rem;
    overflow: hidden;
    position: relative;
    img {
      z-index: 1;
      width: 100%;
      height: auto;
      object-fit: cover;
    }
  }
  #content {
    height: 8rem;
    background-color: #1c1c1c;
    position: relative;
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
  button {
    border-radius: 0;
    position: absolute;
    top: -1.7rem;
    left: 11%;
  }
}
</style>
