<template>
  <Carousel :autoplay="3000" :wrap-around="true" :transition="1000">
    <Slide v-for="item in items" :key="item.id">
      <div class="carousel__item">
        <div class="header__content">
      <div class="container header__content-flex">
        <div class="header__content-left">
          <div class="header__content-top">
            <h3 class="header__content-title">{{item.title}}</h3>
            <p class="header__content-descr">
              {{item.descr}}
            </p>
            <button class="header__content-btn" @click="$emit('modalOpen', true)">{{item.btn}}</button>
          </div>
          <div class="header__content-block">
            <div class="header__content-item">
              <img src="@/assets/img/content-html.svg" alt="" />
              <span class="header__content-name">HTML</span>
            </div>
            <div class="header__content-item">
              <img src="@/assets/img/content-css.svg" alt="" />
              <span class="header__content-name">CSS</span>
            </div>
            <div class="header__content-item">
              <img :src="item.img" alt="" />
              <span class="header__content-name">{{ item.imgName }}</span>
            </div>
          </div>
        </div>
        <div class="header__content-right">
          <img
            src="@/assets/img/header-content.png"
            alt=""
            class="header__content-img"
          />
        </div>
      </div>
    </div>
      </div>
    </Slide>

    <template #addons>
      <Pagination/>
    </template>
  </Carousel>
</template>

<script>
// Carousel start
import { Carousel, Pagination, Slide } from "vue3-carousel";
// Carousel end
export default {
  components: {
    Carousel,
    Slide,
    Pagination
  },
  props: {
    items: {
        typeof: Array,
        required: true
    },
  },
};
</script>