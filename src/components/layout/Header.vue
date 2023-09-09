<script setup>
import  {ref} from 'vue'
const menu = ref([
        {   name: "Plant pots",
            path: "/plant"
        },
        {   name: "Ceramics",
            path: "/ceramics"
        },
        {   name: "Tables",
            path: "/tables"
        },
    ]); 
</script>

<template>
    <header class="header">
        <div class="header-top">
            <div class="header-top-search">
                <img src="/svg/Search.svg" alt="search">
            </div>
            <a href="#" class="header-logo">Avion</a>
            <div class="header-top-right">
                <div class="header-top-right__cart">
                    <a href="#"><img src="/svg/Shopping--cart.svg" alt="basket"></a>
                </div>
                <div class="header-top-right__user">
                    <a href="#"> <img src="/svg/User--avatar.svg" alt="user avatar"></a>
                </div>
            </div>
        </div>
        <div class="header-menu">
            <a class="header-menu__link"
               href="{{element.path}}"
              v-for="(element,i) of menu"
              :key="i"> {{element.name}}
            </a>
        </div>
    </header>
      
</template>

<style lang="scss" scoped>
    .header{
        height: 132px;
        background-color: #fff;
      &-top{
        display: grid;
        border-bottom: 1px solid rgba(0, 0, 0,  .1) ;
        grid-template-columns: repeat(3,1fr);
        height: 70px;
        align-items: center;
        margin: 0 28px;
        &-right{
          display: flex;
          justify-content: end;
          align-items: center;
          &__cart{
            margin-right: 16px;
          }
        }
      }
      &-logo{
        text-align: center;
        text-decoration: none;
        color: #22202E;
        font-size: 24px;
        font-family: "Grava Display", sans-serif;
        &:hover{
          text-decoration: underline;
        }
      }
      &-menu{
        height: 62px;
        display: flex;
        justify-content: center;
        align-items: center;
        &__link{
          margin: 0 22px;
          color: #726E8D;
          text-decoration: none;
          &:hover{
            text-decoration: underline;
          }
        }
      }
    }
</style>