<template>
    <div class="products-container">
        <div class="products">
            <Product
                    v-for="product of products"
                    :key="product.id"
                    :img="product.img"
                    :title="product.title"
                    :price="product.price"
            />
        </div>
        <a href="#" class="products-link">View collection</a>
    </div>

</template>

<script setup>
import Product from '../components/Product.vue';
import {ref} from "vue";
const products = ref([
    {
        id:1,
        img: "../public/img/products/product01.jpg",
        title: "The Dandy chair",
        price: "£250",
    },
    {
        id:2,
        img: "../public/img/products/product02.jpg",
        title: "Rustic Vase Set",
        price: "£155",
    },
    {
        id:3,
        img: "../public/img/products/product03.jpg",
        title: "The Silky Vase",
        price: "£125",
    },
    {
        id:4,
        img: "../public/img/products/product04.jpg",
        title: "The Lucy Lamp",
        price: "£399",
    }
])
</script>

<style lang="scss" scoped>
  .products{
    padding: 0 80px;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    column-gap: 20px;
    margin-bottom: 64px;
    &-container{
      margin-bottom: 56px;
    }
    &-link{
      display: block;
      text-align: center;
      color: #2A254B;
      text-decoration: none;
      &:hover{
        text-decoration: underline;
      }
    }
  }
</style>