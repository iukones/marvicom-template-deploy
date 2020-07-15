<template>
  <div class="post-sidebar ">
    <h2>Publicidad</h2>
    <div class="container-banner-ads">
      <div class="banner-ads">
        <a href="">
          <img src="~/assets/uploads/test.jpg" alt="Ad for SendGrid" />
        </a>
      </div>
      <div class="info-ads">
        <a href="">
          Dra. Oriehta Sánchez Sánchez, nuestra experta en salud nutricional,
          sigue sus consejos y tips, en nuestro blog de salud y en sus redes
          sociales.
        </a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'PostSidebar'
}
</script>

<style lang="scss">
*,
:after,
:before {
  box-sizing: border-box;
}
.post-sidebar {
  h2 {
    margin-top: 1rem;
    margin-bottom: 1rem;
    text-align: center;
  }
  & a {
    color: white;
  }
  & a:hover {
    color: #363636;
  }
}
.container-banner-ads {
  margin: 1.8rem 0 1.8rem 0;
  transform: translateX(-0.5rem);
}
.container-banner-ads:before {
  content: '';
  background: #007c89;
  position: absolute;
  top: -1rem;
  right: -1rem;
  width: 100%;
  height: 100%;
  border-radius: 5px;
  padding-bottom: 1rem;
  opacity: 0.5;
}
.banner-ads {
  margin: 0;
  position: relative;
  & img {
    display: block;
    border-radius: 5px;
    box-shadow: 0 0 30px rgba(16, 14, 23, 0.25);
  }
}
.info-ads {
  font-size: 0.75rem;
  font-weight: 600;
  padding: 1rem 0 2rem 25px;
  margin-left: 1rem;
  white-space: normal;
  position: relative;
}
</style>
