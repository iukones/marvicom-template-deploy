<template>
  <div class="logo-wrapper">
    <div
      :class="{
        'logo-inner': true
      }"
    >
      <img :src="`/logo-frames/withBackground.svg`" />
    </div>
  </div>
</template>
<script>
export default {
  name: 'SiteLogo'
}
</script>
<style lang="scss">
.logo-wrapper {
  position: relative;
  height: 100px;
  overflow: hidden;
  width: 250px;
  @media (max-width: 768px) {
    width: 110px;
  }
  .logo-inner {
    position: absolute;
    // height: 500px;
    img {
      display: block;
      width: 250px;
      height: 100px;
      // margin: 5px;
      max-height: initial;
      @media (max-width: 768px) {
        width: 110px;
      }
    }
  }
}
</style>
