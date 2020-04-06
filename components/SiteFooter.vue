<template>
  <footer class="site-footer">
    {{ $siteConfig.siteName }} &copy; {{ new Date().getFullYear() }} - Todos los
    derechos reservados.
  </footer>
</template>

<script>
export default {
  name: 'SiteFooter'
}
</script>

<style scoped>
footer {
  background: #0f203a;
  padding: 30px 20px;
  text-align: center;
  color: #fff;
  font-size: 1rem;
  transition: 0.5s ease all;
}
</style>
