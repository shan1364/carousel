<template>

<div class="component demo">

<div class="carousel slide demo" id="carousel-demo">
    <ol class="carousel-indicators">
      <li data-target="#carousel-demo" data-slide-to="0" class="active"></li>
      <li data-target="#carousel-demo" data-slide-to="1"></li>
      <li data-target="#carousel-demo" data-slide-to="2"></li>
    </ol>

      <div class="carousel-inner"> <!--幻燈片項目-->
      <div class="carousel-item active">
        <img class="d-block w-100" src="./assets/1.jpg" alt="" />
      </div>
      <div class="carousel-item">
        <img class="d-block w-100" src="./assets/2.jpg" alt="" />
      </div>
      <div class="carousel-item">
        <img class="d-block w-100" src="./assets/3.jpg" alt="" />
      </div>
    </div>

     <a href="#carousel-demo" class="carousel-control-prev" data-slide="prev">
    <span class="carousel-control-prev-icon"></span>
    </a>
    <a href="#carousel-demo" class="carousel-control-next" data-slide="next">
    <span class="carousel-control-next-icon"></span>
    </a>
  </div>


</div>

</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import HelloWorld from './components/HelloWorld.vue'
import $ from 'jquery'
export default {data() {
    return {}
  },
  components: {
    HelloWorld
  },
  created() {
    $(document).ready(() => {
  $('.carousel').carousel({
    interval: 100
  })
})

  }
}


</script>

<style lang="scss">

.component.demo {
  padding: 50px;
}

.carousel.demo .carousel-item {
  height: 400px;
}

.carousel.demo .carousel-item img {
  min-height: 400px;
  max-height: 600px;
  object-fit: cover; 
}

</style>
