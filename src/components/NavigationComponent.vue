<template>
  <div class="position-relative">
    <img src="../assets/imgs/dc-logo-bg.png" alt="" class="dc-bg-logo" />
  </div>
</template>

<script>
export default {
  name: "NavigationComponent",
};
</script>

<style lang="scss" scoped>
.dc-bg-logo {
  z-index: 1;
  position: absolute;
  top: -7rem;
  right: 18rem;
  width: 37rem;
}
</style>
