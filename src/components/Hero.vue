<template>
  <div class="hero">
      <div class="hero-info">
          <HeroInformation
              title="Luxury homeware for people who love timeless design quality"
              description="Shop the new Spring 2022 collection today"
              link="View collection"
          />
      </div>
  </div>
</template>

<script setup>
  import HeroInformation from "./HeroInformation.vue";
</script>

<style lang="scss" scoped>
  .hero{
    padding-right: 80px;
    background: url("public/img/Hero.png");
    height: 704px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    background-size: cover;
     &-img{
       max-width: 100%;
     }
    &-info{
      background: #fff;
      max-width: 630px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      &__title{
        font-family: 'Grava Display',serif;
        font-weight: 400;
        line-height: 1.5;
      }
      &-text{
      }
      &__discription{
        color:#585676;
        font-size: 18px;
      }
      &-link{
        //margin-top: 157px;
        color:#2a2548;
        text-decoration: none;
        &:hover{
          text-decoration: underline;
        }
      }
    }
  }
</style>