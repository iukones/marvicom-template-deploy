<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="Sobre nosotros"
      subtitle="Nuestra Misión, Visión y Objetivos en Marvicom comunicaciones"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <div class="content">
      <!-- component -->
      <section>
        <div class="container">
          <div class="content__title">
            <h1>
              Marvicom prensa y revista digital.
            </h1>
            <p>
              Nuestro proyecto ambicioso de canal digital de comunicación, el
              cual se ha estructurado en el formato de revista digital.
            </p>
          </div>
          <div class="divided"></div>

          <div class="main__content__card">
            <div class="blocks">
              <div class="blocks__content">
                <figure class="blocks__image">
                  <div class="blocks__images__content">
                    <img
                      src="../assets/uploads/about-1.jpg"
                      alt="image example"
                    />
                    <div class="image__overlay"></div>
                  </div>
                  <figcaption class="image__card">
                    <div class="card__text">
                      <p>
                        Lorem ipsum dolor sit amet consectetur, adipisicing
                        elit. Voluptatem vitae, expedita architecto obcaecati
                        laudantium eius sit adipisci excepturi aut, inventore,
                        vel quasi ipsam beatae sequi. Sed excepturi ipsa minima
                        suscipit!
                      </p>
                    </div>
                  </figcaption>
                </figure>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>
<script>
// import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `Nosotros | ${this.$siteConfig.siteName}`
    }
  }
  // components: { QuoteCard }
}
</script>
<style lang="scss">
.blocks {
  border: 1px solid red;
  position: relative;
  height: auto;
  padding: 17px;
  outline: none;
  box-shadow: inset 0 0 0 1px rgba(128, 128, 128, 0);
  -webkit-transition: box-shadow 0.2s ease-in-out;
  -moz-transition: box-shadow 0.2s ease-in-out;
  -ms-transition: box-shadow 0.2s ease-in-out;
  -o-transition: box-shadow 0.2s ease-in-out;
  transition: box-shadow 0.2s ease-in-out;
  @media (min-width: 640px) {
    margin-top: 0 !important;
  }
  & .blocks__image {
    display: block;
    position: relative;
    margin: 0;
    & .blocks__images__content {
      overflow: visible;
      width: 90%;
      position: relative;
      max-width: initial;
    }
  }
}
</style>
