<template>
  <header class="header">
    <nav class="nav">
      <div class="container header__nav">
        <a class="header__logo" href="#">
          <span class="line"></span>
          <span class="my">MY</span>
          <span class="work">WORK</span>
        </a>
        <div
          class="header__burger"
          @click="activeBtn"
          :class="{ active: active }"
        >
          <span class="header__burger-line"></span>
          <span class="header__burger-line"></span>
          <span class="header__burger-line"></span>
        </div>
        <ul class="header__nav-list" :class="{ active: active }">
          <li>
            <a href="#about" class="header__nav-link">
              Обо мне
            </a>
          </li>
          <li>
            <a href="#works" class="header__nav-link">
              Мои работы
            </a>
          </li>
          <li>
            <button class="header__nav-link bg" @click="openModal = !openModal">
              Заказать
            </button>
          </li>
          <li>
            <a href="tel:+998998662364" class="header__nav-img"
              ><img src="@/assets/img/call.svg" alt=""
            /></a>
          </li>
        </ul>
        <Modal
          v-show="openModal"
          :openModal="openModal"
          @closeModal="closeModal"
        />
      </div>
    </nav>
    <div class="slider" 
      data-aos="fade-down"
      data-aos-duration="1000">
      <CarouselItem 
        :items="items"
        @modalOpen="openModal = $event"
      />
    </div>
  </header>
</template>

<script>
import Modal from "@/components/Modal.vue";
import CarouselItem from "@/components/CarouselItem.vue";

export default {
  components: {
    Modal,
    CarouselItem
  },
  data() {
    return {
      active: false,
      openModal: false,
      items: [
        {
          id: 1,
          title: "My beginning",
          descr: "Self-development and training in the training center",
          btn: "GET STARTED NOW",
          img: require("@/assets/img/content-vue.svg"),
          imgName: "VUE JS"
        }, 
        {
          id: 1,
          title: "My beginning",
          descr: "Self-development and training in the training center",
          btn: "GET STARTED NOW",
          img: require("@/assets/img/content-bootstrap.svg"),
          imgName: "BOOTSTRAP 5"
        }  
      ]
    };
  },
  methods: {
    activeBtn() {
      this.active = !this.active;
    },
    closeModal(status) {
      this.openModal = status;
    },
  },
};
</script>

<style>
</style>