<template>
  <Header></Header>
  <Banner></Banner>
  <CarrouselCategories></CarrouselCategories>
  <router-view />
  <Footer></Footer>
</template>
<script>
import Header from "@/components/Header.vue";
import Banner from "@/components/Banner";
import CarrouselCategories from "@/components/CarrouselCategories";
import Footer from "@/components/Footer";
export default {
  components: {
    Header,
    Banner,
    CarrouselCategories,
    Footer,
  },
};
</script>

 