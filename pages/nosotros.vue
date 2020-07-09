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
              Nuestro proyecto ambicioso de un canal de comunicación, el cual se
              ha estructurado en el formato de revista digital.
            </p>
          </div>
          <div class="divided"></div>

          <div class="main__content__card">
            <div class="cover-story">
              <div class="cover-splash">
                <picture>
                  <source
                    srcset="
                      ../assets/uploads/origami@2x.jpg 1590w,
                      // eslint-disable-next-line prettier/prettier
                      ../assets/uploads/origami.jpg 795w"
                    sizes="100vw"
                    media="( min-width: 34em )"
                  />
                  <img
                    class="intro-art"
                    src="../assets/uploads/origami-sm.jpg"
                    alt="Rawr."
                  />
                </picture>

                <div class="intro-blur" role="presentation">
                  <img src="../assets/uploads/origami.jpg" alt="" />
                </div>

                <div class="blurb">
                  <h2 class="hed hed-blurb">
                    <span class="icon">
                      <fa :icon="['fas', 'users']" />
                    </span>
                    <a href="#">
                      <q>
                        It’s not terrible, but it can be lone to be theking.
                      </q>
                    </a>
                  </h2>
                  <p>
                    In a new interview, Chadley Tyrannosaurus opens up about
                    life, laughter, and love as predator.
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="main__content__card">
            <div class="detail__text">
              <div class="text__content">
                <div class="blurb">
                  <h2 class="hed hed-blurb">
                    <span class="icon">
                      <fa :icon="['fas', 'project-diagram']" />
                    </span>
                    <a href="#">
                      <q>
                        It’s not terrible, but it can be lone to be theking.
                      </q>
                    </a>
                  </h2>
                  <p>
                    In a new interview, Chadley Tyrannosaurus opens up about
                    life, laughter, and love as predator.
                  </p>
                </div>
              </div>
              <div class="text__content">
                <div class="blurb">
                  <h2 class="hed hed-blurb">
                    <span class="icon">
                      <fa :icon="['fas', 'lightbulb']" />
                    </span>
                    <a href="#">
                      <q>
                        It’s not terrible, but it can be lone to be theking.
                      </q>
                    </a>
                  </h2>
                  <p>
                    In a new interview, Chadley Tyrannosaurus opens up about
                    life, laughter, and love as predator.
                  </p>
                </div>
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
<style lang="scss" scoped>
.container {
  width: 100%;
  @media (min-width: 1280px) {
    .container {
      max-width: 1280px;
    }
  }
  @media (min-width: 1024px) {
    .container {
      max-width: 1024px;
    }
    .main__content__card {
      max-width: 80%;
    }
  }
  @media (min-width: 768px) {
    .container {
      max-width: 768px;
    }
  }
  @media (min-width: 640px) {
    .container {
      max-width: 640px;
    }
  }
}
.content {
  padding: 3.75em 0;
}
.content__title {
  & h1 {
    -webkit-font-kerning: normal;
    font-kerning: normal;
    font-variant-ligatures: common-ligatures contextual discretionary-ligatures;
    font-feature-settings: 'kern', 'liga', 'clig', 'calt', 'dlig';
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    display: block;
    color: #212b35;
    line-height: 1.2142857143;
    letter-spacing: -0.025em;
    text-align: center;
    font-size: 1.8rem;
    font-family: 'Montserrat', sans-serif;
    @media (min-width: 768px) {
      font-size: 2rem;
    }
  }
  & h2 {
    text-align: center;
    font-family: 'Montserrat', sans-serif;
  }
  & p,
  .text__bottom {
    font-size: 1rem;
    margin-bottom: 0.5rem;
    color: #637381;
    text-align: center;
    padding: 0 1.5rem 0 1.5rem;
    margin-top: 0.5rem;
    @media (min-width: 1024px) {
      padding: 0 15.5rem 0 15.5rem;
      font-size: 1.3rem;
    }
    @media (min-width: 768px) {
      padding: 0 8rem 0 8rem;
      font-size: 1.3rem;
    }
  }
  & .text__bottom {
    @media (min-width: 1024px) {
      padding: 0 10rem 0 10rem;
      font-size: 1.3rem;
    }
    @media (min-width: 768px) {
      padding: 0 5rem 0 5rem;
      font-size: 1.3rem;
    }
  }
  &.bottom {
    margin-top: 5rem;
  }
}
.divided {
  width: 6rem;
  opacity: 0.75;
  margin: 3rem auto 1rem auto;
  height: 0.25rem;
  background-color: #c3dafe;
  border-radius: 0.25rem;
}
.main__content__card {
  padding: 0 2rem 0 2rem;
  margin: 3rem auto 5rem auto;
  max-width: 100%;
  & .icon {
    margin-left: 1.5rem;
    color: burlywood;
  }
  /*
  Cover story
  */
  .blurb,
  .blurb:before,
  .blurb:after {
    background-color: #3b3e93;
    background-color: rgba(59, 62, 147, 0.7);
  }

  .blurb {
    background-color: #3b3e93;
    background-color: rgba(59, 62, 147, 0.7);
    background-image: radial-gradient(
      circle at 100% 100%,
      rgba(255, 255, 255, 0.5),
      rgba(0, 0, 0, 0.5) 75%
    );
    color: #fff;
    padding: 3em;
    position: relative;
    z-index: 100;
  }

  .blurb:before,
  .blurb:after {
    content: '';
    height: 1em;
    position: absolute;
    width: 50%;
  }

  .blurb:before {
    left: 0;
    top: -1em;
  }

  .blurb:after {
    right: 0;
    bottom: -1em;
  }

  .blurb a {
    color: inherit;
  }

  .blurb q:before,
  .blurb q:after {
    display: inline-block;
    text-decoration: none;
    text-indent: 0;
  }

  .blurb .hed {
    font-size: 2.5em;
    /* 40/16 */
    line-height: 1.05;
    /* 42/40 */
    margin: 0 0 0.25em;
    text-indent: -0.75em;
    color: #fff !important;
  }

  .blurb p {
    font-size: 1.5em;
    /* 24/16 */
    line-height: 1.25;
    /* 30/24 */
    margin: 0;
  }

  .intro-art {
    display: block;
  }

  .intro-blur {
    display: none;
    overflow: hidden;
    z-index: 1;
  }

  .intro-blur img {
    // transform: scale(2);
    // filter: blur(17px);
    max-width: 60%;
  }

  img {
    max-width: 100%;
  }
  .intro-blur {
    display: none;
  }
  .blurb {
    padding: 1.5em;
  }
  .blurb .hed {
    font-size: 1.5em;
    /* 40/16 */
  }
  .blurb p {
    font-size: 1.2em;
    /* 20/16 */
  }
}
.text__content {
  margin-bottom: 4.5rem;
}

@media (min-width: 30em) {
  .blurb {
    padding: 2em;
  }
  .blurb .hed {
    font-size: 2em;
    /* 40/16 */
  }
}
@media (min-width: 40em) {
  .blurb {
    padding: 3em;
  }
  .blurb .hed {
    font-size: 2.5em;
    /* 40/16 */
  }
  .blurb p {
    font-size: 1.5em;
    /* 24/16 */
  }
}
@media (min-width: 50em) {
  .cover-splash {
    display: grid;
    grid-column-gap: 2.5%;
    grid-template-columns: [content-start] repeat(5, minmax(1em, 1fr)) [content-end];
    /* & picture {
      display: content !important;
    } */
    .cover-story .hed-section {
      grid-column: 1 / span 3;
    }
    .cover-story .more {
      grid-column: 5;
    }
    .intro-blur,
    .blurb {
      grid-row: 1;
    }
    @supports (display: grid) {
      .intro-blur {
        display: block;
        grid-column: 1 / -1;
      }
    }
    .blurb {
      align-self: center;
      grid-column: 3 / -1;
      justify-self: end;
      max-width: 30em;
      position: relative;
      z-index: 100;
    }
    .blurb .hed,
    .blurb p {
      max-width: inherit;
    }
  }
  .intro-art {
    display: none !important;
    /* height: 100%;
    grid-column: 1 / span 4;
    object-fit: cover;
    z-index: 10; */
  }
  .text__content {
    // background-color: dodgerblue;
    color: white;
    // padding: 1rem;
    height: auto;
  }

  .detail__text {
    max-width: 1200px;
    margin: 0 auto;
    display: grid;
    grid-gap: 1rem;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  }
}
</style>
