<template>
    <div class="hero-info"
         :style="{backgroundColor: background}">
        <div class="hero-info-text">
            <h2
                class="hero-info__title"
                :style="{color:colorTitle}">{{title}}
            </h2>
                <span
                    class="hero-info__description"
                    :style="{color:colorDescription}">{{description}}
                </span>
            <a href="#"
               :style="{color:colorLink}"
               class="hero-info-link">{{link}}
            </a>
        </div>

    </div>

</template>

<script setup>

const props = defineProps({
      title:{
          type:String,
          required:false

      },
      description:{
          type:String,
          required:false

      },
      link:{
          type:String,
          required:false
      },
    colorTitle:{
        type:String,
        default:''
    },
    colorLink:{
        type:String,
        default:'#2A254B'
    },
    colorDescription:{
        type:String,
        default: '#585676'
    },
    background:{
        type:String,
        default:'#fff'
    }
  })
</script>

<style lang="scss" scoped>
.hero{
    &-img{
        max-width: 100%;
    }
    &-info{
        background: #fff;
        //min-height: 199px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        &__title{
            //padding: 30px 64px 0;
            font-family: 'Grava Display',serif;
            font-weight: 400;
            line-height: 1.5;
            font-size: 34px;
        }
        &-text{
            max-width:587px;
            padding-left: 64px;
        }
        &__discription{
            color:#585676;
            font-size: 18px;
        }
        &-link{
            margin: 156px 0 63px;
            text-decoration: none;
            width: 195px;
            height: 56px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(249, 249, 249, 0.15);
            cursor: pointer;
            &:hover{
                background: rgba(249, 249, 249, 0.30);
                text-decoration: underline;
            }
        }
    }
}
</style>