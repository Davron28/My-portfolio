<template>
  <div class="accordion__item" v-for="item in accordionItems" :key="item.id">
    <h2 class="accordion__title" @click="toggleAccordion(item)">
        <button class="accordion__btn">
            <img :src="item.img" alt="">
            <span :class="item.btn ? 'color' : ''">{{item.name}}</span>
            <span class="icon__arrow-top" :class="item.btn ? 'rotate' : ''"></span>
        </button>
    </h2>
    <p class="accordion__nobody" :class="item.btn ? 'accordion__body' : ''">{{ item.descr }}</p>
  </div>
</template>

<script>
import {ref} from "vue"
export default {
    setup() {
        const accordionItems = ref([
                {
                    id: 1,
                    name: "HTML",
                    descr: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Venenatis felis dui quis eget suspendisse rutrum orci. Elementum, ultrices dictum cras sit volutpat morbi adipiscing ut. Convallis faucibus ligula blandit enim. Accumsan est ",
                    img: require("@/assets/img/accordion-html.svg"),
                    btn: false
                },
                {
                    id: 2,
                    name: "CSS",
                    descr: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Venenatis felis dui quis eget suspendisse rutrum orci. Elementum, ultrices dictum cras sit volutpat morbi adipiscing ut. Convallis faucibus ligula blandit enim. Accumsan est ",
                    img: require("@/assets/img/accordion-css.svg"),
                    btn: false
                },
                {
                    id: 3,
                    name: "BOOTSTRAP",
                    descr: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Venenatis felis dui quis eget suspendisse rutrum orci. Elementum, ultrices dictum cras sit volutpat morbi adipiscing ut. Convallis faucibus ligula blandit enim. Accumsan est ",
                    img: require("@/assets/img/accordion-bootstrap.svg"),
                    btn: false
                },
                {
                    id: 4,
                    name: "JavaScript",
                    descr: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Venenatis felis dui quis eget suspendisse rutrum orci. Elementum, ultrices dictum cras sit volutpat morbi adipiscing ut. Convallis faucibus ligula blandit enim. Accumsan est ",
                    img: require("@/assets/img/accordion-js.svg"),
                    btn: false
                },
                {
                    id: 5,
                    name: "Vue JS",
                    descr: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Venenatis felis dui quis eget suspendisse rutrum orci. Elementum, ultrices dictum cras sit volutpat morbi adipiscing ut. Convallis faucibus ligula blandit enim. Accumsan est ",
                    img: require("@/assets/img/accordion-vue.svg"),
                    btn: false
                },
            ]) 
        function toggleAccordion(item) {
            if(!item.btn) {
                accordionItems.value.forEach(el => el.btn = false)
            }
            item.btn = !item.btn
        }
        return {
            accordionItems,
            toggleAccordion
        }
    }
}
</script>

<style>

</style>