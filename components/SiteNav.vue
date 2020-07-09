<template>
  <nav
    class="navbar has-shadow is-fixed-top"
    role="navigation"
    aria-label="main navigation"
  >
    <div class="navbar-brand">
      <nuxt-link class="navbar-item" to="/">
        <site-logo v-if="$siteConfig.logo === 'logo-component'" />
        <img
          v-else
          :src="$siteConfig.logo"
          :alt="$siteConfig.siteName"
          class="logo"
        />
      </nuxt-link>
      <hamburger-button @click="active = !active" />
    </div>

    <div
      :class="{
        'navbar-menu': true,
        'is-active': active
      }"
    >
      <ul class="navbar-end">
        <li
          v-for="item in $siteConfig.mainMenu"
          :key="item.link"
          class="navbar-item"
          @click="active = false"
        >
          <component
            :is="item.link.startsWith('http') ? 'a' : 'nuxt-link'"
            :href="item.link"
            :to="item.link"
            :target="item.target ? item.target : '_self'"
          >
            {{ item.name }}
          </component>
        </li>
        <li class="navbar-item site-search-wrapper">
          <site-search />
        </li>
      </ul>
    </div>
  </nav>
</template>
<script>
import SiteSearch from '~/components/SiteSearch'
import HamburgerButton from '~/components/HamburgerButton'
export default {
  name: 'SiteNav',
  components: { SiteSearch, HamburgerButton },
  data() {
    return {
      active: false
    }
  }
}
</script>
<style lang="scss" scoped>
.navbar.is-fixed-top {
  z-index: 1000;
}
.has-shadow {
  box-shadow: 0 10px 25px -19px rgba(51, 67, 84, 0.68),
    0 4px 6px -2px rgba(0, 0, 0, 0.05) !important;
}
.navbar-item img {
  max-height: 2rem;
}
.site-search-wrapper {
  transform: translateX(5px);
  @media (max-width: 1023px) {
    display: none !important;
  }
}
.navbar-burger {
  height: auto;
  width: 5.25rem;
}

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
.navbar-menu {
  @media (max-width: 1023px) {
    height: 90vh;
    padding: 3.5rem 0;
  }
}
.navbar-menu a {
  display: block;
  font-weight: 600;
  line-height: 24px;
  font-size: 13px;
  color: #007c89;
  text-transform: uppercase;
  @media (max-width: 1023px) {
    font-size: 1.5rem;
    padding: 1rem;
  }
}
.navbar-menu a:hover {
  color: #212b35 !important;
}
.navbar-item {
  @media (max-width: 1023px) {
    display: flex;
    justify-content: center;
  }
}
</style>
