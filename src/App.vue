<template>
  <Header />
  <Main />
  <Footer />
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Main from './components/Main.vue';

export default {  
  components: {
    Header,
    Footer,
    Main,
  }, 
}

</script>


<style lang="scss" scoped>

@import "./assets/scss/general.scss";

#app {
	font-family: $main_font;
}
#secondary-nav,
footer li {
	font-family: $lighter_font;
}

</style>
