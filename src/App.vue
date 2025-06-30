<template>
  <Header />
  <HeroSection />
  <AboutSection />
  <Projects />
  <Reviews />
  <Footer />
</template>

<script>
import Header from './components/layout/Header.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import Projects from './components/Projects.vue'
import Reviews from './components/Reviews.vue'
import Footer from './components/layout/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    HeroSection,
    AboutSection,
    Projects,
    Reviews,
    Footer
  }
}
</script>

<style lang="scss">
@use "./assets/sass/main.scss";
</style>