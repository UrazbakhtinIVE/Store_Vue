<template>
    <div class="container">
        <Header/>
        <Hero/>
        <AboutBrand/>
        <Products/>
        <Idees/>
    </div>
</template>

<script setup>
import Header from './components/layout/Header.vue'
import Hero from "./components/Hero.vue";
import AboutBrand from  "./components/AboutBrand.vue";
import Products from "./components/Products4column.vue";
import Idees from "./components/Ideas.vue";
</script>



<style lang="scss">
@import url('https://fonts.cdnfonts.com/css/satoshi');
@import url('https://fonts.cdnfonts.com/css/grava');

*{
    box-sizing: border-box;
  }

//font-family: 'Grava Display', sans-serif;

  body{
    margin: 0;
    padding: 0;
    font-family: 'Satoshi', sans-serif;
    font-size: 16px;
  }
  img{
      max-width: 100%;
  }
  .container{
    max-width: 1140px;
    margin: 0 auto;
  }
</style>
