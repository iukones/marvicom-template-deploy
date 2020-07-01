<template>
  <div id="home-page" class="page-wrapper home-page">
    <site-hero :title="title" :subtitle="subtitle" :image="featureImage">
      <button
        class="button is-primary is-medium is-inverted is-outlined"
        @click="$eventBus.$emit('modal-triggered', 'newsletter-modal')"
      >
        Suscribirse
      </button>
    </site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <!-- All Posts -->
        <h2 class="subtitle__post">
          Noticias recientes.
        </h2>
        <posts-grid />
      </template>
      <template v-slot:sidebar>
        <post-sidebar />
      </template>
    </main-section>
    <news-letter-form-modal />
  </div>
</template>

<script>
import { mapState } from 'vuex'
import { setPageData } from '../helper'
import NewsLetterFormModal from '~/components/NewsLetterFormModal'
import PostSidebar from '~/components/PostSidebar'

export default {
  name: 'HomePage',
  head() {
    return {
      title: `Home | ${this.$siteConfig.siteName}`
    }
  },
  components: {
    NewsLetterFormModal,
    PostSidebar
  },
  computed: {
    ...mapState(['title', 'subtitle', 'featureImage'])
  },
  fetch({ store, params }) {
    setPageData(store, { slug: 'home' })
  }
}
</script>

<style lang="scss" scoped>
.home-page .under-subtitle {
  border-top: none;
}
.subtitle__post {
  font-family: 'Montserrat', sans-serif;
  color: #0f203a;
  letter-spacing: normal;
  margin-left: 0;
  font-size: 1.5rem;
  @media (min-width: 1024px) {
    margin: 1.5rem;
    font-size: 2rem;
    letter-spacing: 1.5px;
  }
}
iframe {
  min-height: 315px !important;
  max-width: 100% !important;
  margin-top: 2rem;
  margin-bottom: 2rem;
}
</style>
