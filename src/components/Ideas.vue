<template>
      <div class="ideas">
          <div class="ideas-info">
              <HeroInformation
                title="It started with a small idea"
                description="A global brand with local beginnings, our story begain in a small studio in South London in early 2014"
                link="View collection"
                colorTitle="#fff"
                colorDescription="#fff"
                background="#2A2548"
                colorLink="#fff"
              />
          </div>
            <img src="../../public/img/room.jpg" alt="room">
      </div>
</template>

<script setup>
import HeroInformation from "./HeroInformation.vue";
</script>

<style lang="scss" scoped>
  .ideas{
    //padding: 0 80px;
    //margin-bottom: 68px;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    column-gap: 16px;
  }
</style>