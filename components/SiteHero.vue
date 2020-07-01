<template>
  <section :class="`hero is-medium hero-theme-${computedTheme}`">
    <img
      class="hero-bg-img"
      :src="responsiveImage.src"
      :lazy="true"
      :srcset="responsiveImage.srcSet"
    />
    <div class="hero-body">
      <div class="container">
        <h1 class="title animated fadeInUp">
          {{ title }}
        </h1>
        <h2 class="subtitle animated fadeInUp slower">
          {{ subtitle }}
        </h2>
        <br />
        <div
          v-if="$slots.default"
          class="under-subtitle animated fadeInDown slower"
        >
          <slot />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'SiteHero',
  props: {
    title: { type: String, default: '' },
    span: { type: String, default: '' },
    subtitle: { type: String, default: '' },
    image: { type: String, default: '' },
    color: { type: String, default: '#469af0' },
    theme: { type: String, default: '' }
  },
  computed: {
    responsiveImage() {
      if (this.image.indexOf('/uploads') === 0) {
        return require(`~/assets${this.image}`)
      }
      return { src: this.image, srcSet: '' }
    },
    computedTheme() {
      if (this.theme === '' && this.$siteConfig.hero.theme) {
        return this.$siteConfig.hero.theme
      }
      return this.theme || 'mist'
    }
  }
}
</script>

<style lang="scss" scoped>
.hero {
  margin-top: 6rem;
  background-size: cover !important;
  background-position: center;
  text-align: center;
  overflow: hidden;
  position: relative;
  height: 80vh;
  @media (max-width: 768px) {
    height: 60vh;
  }
}

.container {
  @media (max-width: 768px) {
    margin-top: 3rem;
  }
}

.title {
  font-family: 'Montserrat', sans-serif;
  font-weight: 800;
  // letter-spacing: 3px;
  line-height: 70px;
  span {
    color: #ff3366;
  }
  @media (min-width: 768px) {
    font-size: 3.2rem;
  }
  @media (max-width: 768px) {
    line-height: initial;
  }
}
.subtitle,
.under-subtitle {
  font-family: 'Open Sans', sans-serif;
  padding: 0;
  margin: 0;
}
.subtitle {
  font-size: 20px;
  line-height: 30px;
  margin-bottom: 0 !important;
  padding-top: 1rem;
  font-weight: 400 !important;
  @media (min-width: 1024px) {
    padding-left: 25rem;
    padding-right: 25rem;
  }
}
.under-subtitle {
  display: inline-block;
  font-size: 1rem;
  border-top: 2px solid $primary;
  padding-top: 5px;
  letter-spacing: 1px;
}
.opti-image {
  opacity: 0;
}
.opti-image-loaded {
  opacity: 0.12;
  animation: blurIn 4.5s ease;
}
</style>
<style lang="scss">
.hero {
  .hero-bg-img {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    object-fit: cover;
    width: 100%;
    height: 100%;
  }
  .opti-image {
    opacity: 0;
  }
  .opti-image-loaded {
    opacity: 1;
  }
}
.hero-theme-mist {
  .hero-bg-img {
    filter: grayscale(1);
  }
  .opti-image-loaded {
    opacity: 0.12;
    animation: blurInGrayscale 4.5s ease;
  }
}
.hero-theme-dark,
.hero-theme-light {
  &.hero:after {
    content: '';
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0, 0, 0, 0.65);
    position: absolute;
  }
  .hero-body {
    position: relative;
    z-index: 2;
  }
}
.hero-theme-dark {
  .title,
  .subtitle,
  .under-subtitle,
  .under-subtitle strong {
    color: white;
  }
}
.hero-theme-light.hero {
  &:after {
    background: rgba(255, 255, 255, 0.6);
  }
  .title,
  .subtitle,
  .under-subtitle,
  .under-subtitle strong {
    text-shadow: 1px 1px 2px white;
  }
}
</style>
