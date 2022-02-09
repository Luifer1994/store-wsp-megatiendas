<template>
  <section class="hero">
    <div class="container">
      <div class="row">
        <div class="col-lg-12">
          <Carousel :autoplay="10000" :wrap-around="true">
            <Slide v-for="slide in 2" :key="slide">
              <img
                src="https://bolcereales.com.ar/wp-content/uploads/2021/04/beneficios-de-las-verduras.jpg"
                class="img-fluid rounded"
                alt="..."
              />
            </Slide>
          </Carousel>

          <div class="hero__search mt-2 p-2">
            <div class="hero__search__form">
              <form action="#">
                <input
                  type="text"
                  style="border-radius: 7px"
                  placeholder="Buscar..."
                />
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide } from "vue3-carousel";

export default {
  name: "App",
  components: {
    Carousel,
    Slide,
  },
  data() {
    return {
      settings: {
        itemsToShow: 1,
        snapAlign: "center",
      },
      // breakpoints are mobile first
      // any settings not specified will fallback to the carousel settings
      breakpoints: {
        // 700px and up
        700: {
          itemsToShow: 3.5,
          snapAlign: "center",
        },
        // 1024 and up
        1024: {
          itemsToShow: 5,
          snapAlign: "start",
        },
      },
    };
  },
  // carousel settings
};
</script>

<style>
.carousel__item {
  min-height: 300px;
  width: 100%;
  color: rgba(255, 255, 255, 0);
  font-size: 20px;
  border-radius: 7px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>