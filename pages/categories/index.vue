<template>
  <div id="categories-page" class="page-wrapper categories-page">
    <site-hero
      title="Categorias"
      subtitle="Busca tu sección favorita en nuestras categorias."
      image="/uploads/category-edit.jpg"
    />
    <main-section theme="one-column">
      <categories-grid />
    </main-section>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: `Categorias | ${this.$siteConfig.siteName}`
    }
  }
}
</script>
