<template>
    <div class="about-brand">
        <h3 class="about-brand__title"></h3>
            <div class="about-brand-elements">
                <div class="about-brand-element"
                    v-for="(element,i) of aboutBrands"
                     :key="i"
                >
                    <img
                        :src="element.img"
                        :alt="element.title"
                        class="about-brand-element__img"
                    >
                    <span class="about-brand-element__title">{{element.title}}</span>
                    <span class="about-brand-element__description">{{element.description}}</span>
                </div>
            </div>
    </div>
</template>

<script setup>
    import {ref} from 'vue'
    const  aboutBrands = [
        {
            img: '/svg/aboutBrand-icon_01.svg',
            title: 'What makes our brand different',
            description:'Order before 3pm and get your order the next day as standard'
        },
        {
            img: '/svg/aboutBrand-icon_02.svg',
            title: 'Made by true artisans',
            description:'Handmade crafted goods made with real passion and craftmanship'
        },
        {
            img: '/svg/aboutBrand-icon_03.svg',
            title: 'Unbeatable prices',
            description:'For our materials and quality you won’t find better prices anywhere'
        },
        {
            img: '/svg/aboutBrand-icon_04.svg',
            title: 'Recycled packaging',
            description: 'We use 100% recycled to ensure our footprint is more manageable'
        }
    ]
</script>

<style lang="scss" scoped>
  .about-brand{
    padding: 80px 80px 130px 80px;
    &__title{
      text-align: center;
      font-size: 24px;
      color: #2A2548;
      margin: 0 0 84px;
      font-weight: 400;
    }
      &-elements{
          display: grid;
          grid-template-columns: repeat(4, 210px);
          justify-content: space-between;
      }
      &-element{
          color: #2A2548;
          &__img{
              display: block;
              margin-bottom: 12px;
          }
          &__title{
              margin: 0 0 12px 0;
              font-size: 20px;
          }
          &__description{
              font-size: 16px;
              line-height: 1.5;
          }
      }
  }
</style>