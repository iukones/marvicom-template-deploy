<template>
  <footer class="site-footer">
    <div class="container">
      <div class="columns">
        <div class="column">
          <p class="social-copy">
            Siguenos en:
          </p>
          <div class="footer-social">
            <a href="https://www.facebook.com/marvicom.live/">
              <fa :icon="['fab', 'facebook']" />
            </a>
            <a href="https://www.youtube.com/channel/UCbudQsFN8fQI065eiorLVzw">
              <fa :icon="['fab', 'youtube']" />
            </a>
          </div>
          <p class="footer-copy">
            {{ $siteConfig.siteName }} &copy; {{ new Date().getFullYear() }}
            - Todos los derechos reservados.
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'SiteFooter'
}
</script>

<style scoped>
footer {
  background: #344258;
  padding: 30px 20px;
  text-align: center;
  color: #fff;
  font-size: 1rem;
  transition: 0.5s ease all;
}
.footer-copy {
  text-align: center;
  padding: 10px 0;
}
.social-copy {
  padding-top: 10px;
  font-weight: bold;
}
.footer-social {
  text-align: center;
  padding: 10px 0;
}
.footer-social a {
  padding: 0 6px;
  color: #fafafa;
  font-size: 2rem;
  transition: all 0.3s ease-in-out;
}
.footer-social a:hover {
  color: #aec9cb !important;
}
</style>
