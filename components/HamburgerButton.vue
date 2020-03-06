<template functional>
  <a
    role="button"
    class="navbar-burger"
    aria-label="menu"
    aria-expanded="false"
    @click="listeners.click"
  >
    <span aria-hidden="true"></span>
    <span aria-hidden="true"></span>
    <span aria-hidden="true"></span>
  </a>
</template>
<style lang="scss" scoped>
.navbar-burger span {
  height: 3px !important;
  width: 28px !important;
}

.navbar-burger span:nth-child(1) {
  top: calc(50% - 8px) !important;
}

.navbar-burger span:nth-child(3) {
  top: calc(50% + 6px) !important;
}
</style>
