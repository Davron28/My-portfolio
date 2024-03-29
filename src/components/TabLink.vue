<template>
  <h2 class="main__work-title" id="works">Мои Работы</h2>
  <div class="container">
    <div class="main__work" data-aos="fade-up"
     data-aos-anchor-placement="bottom-bottom">
      <ul class="main__work-left">
        <li>
          <a href="#!" class="main__work-btn" :class="{active: tabs === 'tab1'}" @click="tabs='tab1'">NIKE</a>
        </li>
        <li>
          <a href="#!" class="main__work-btn" :class="{active: tabs === 'tab2'}" @click="tabs='tab2'">SIMPLE</a>
        </li>
        <li>
          <a href="#!" class="main__work-btn" :class="{active: tabs === 'tab3'}" @click="tabs='tab3'">VUE CINEMA</a>
        </li>
        <li>
          <a href="#!" class="main__work-btn" :class="{active: tabs === 'tab4'}" @click="tabs='tab4'">PLANT SHOP</a>
        </li>
      </ul>
      <div class="main__work-right">
        <div class="main__work-item" :class="{active: tabs === 'tab1'}">
          <div class="main__work-item__left">
            <img src="@/assets/img/nike-work.png" alt="" />
          </div>
          <div class="main__work-item__right">
            <h2 class="main__work-item__title">NIKE Layout</h2>
            <p class="main__work-item__text">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Orci,
              mauris neque, gravida amet diam cum nisl enim. Vestibulum, risus,
              maecenas et nisi lobortis malesuada vel. Neque, sem tellus sed a,
              enim egestas. Mi mi id amet, lorem vitae lectus risus diam nunc.
              Eget nunc eget lectus amet feugiat lobortis sit sit non eu. Nunc,
              mauris viverra quis sapien quam. Non parturient sed
            </p>
            <a href="https://davron28.github.io/Nike-New/" target="_blank"  class="main__work-item__btn">Посетить сайт</a>
          </div>
        </div>
        <div class="main__work-item" :class="{active: tabs === 'tab2'}">
          <div class="main__work-item__left">
            <img src="@/assets/img/open-shop-work.png" alt="" />
          </div>
          <div class="main__work-item__right">
            <h2 class="main__work-item__title">Simple Layout</h2>
            <p class="main__work-item__text">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Orci,
              mauris neque, gravida amet diam cum nisl enim. Vestibulum, risus,
              maecenas et nisi lobortis malesuada vel. Neque, sem tellus sed a,
              enim egestas. Mi mi id amet, lorem vitae lectus risus diam nunc.
              Eget nunc eget lectus amet feugiat lobortis sit sit non eu. Nunc,
              mauris viverra quis sapien quam. Non parturient sed
            </p>
            <a href="https://davron28.github.io/SimpleIt/" target="_blank" class="main__work-item__btn">Посетить сайт</a>
          </div>
        </div>
        <div class="main__work-item" :class="{active: tabs === 'tab3'}">
          <div class="main__work-item__left">
            <img src="@/assets/img/cinema-work.png" alt="" />
          </div>
          <div class="main__work-item__right">
            <h2 class="main__work-item__title">Vue-Cinema Layout</h2>
            <p class="main__work-item__text">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Orci,
              mauris neque, gravida amet diam cum nisl enim. Vestibulum, risus,
              maecenas et nisi lobortis malesuada vel. Neque, sem tellus sed a,
              enim egestas. Mi mi id amet, lorem vitae lectus risus diam nunc.
              Eget nunc eget lectus amet feugiat lobortis sit sit non eu. Nunc,
              mauris viverra quis sapien quam. Non parturient sed
            </p>
            <a href="https://davron28.github.io/cinema/" target="_blank" class="main__work-item__btn">Посетить сайт</a>
          </div>
        </div>
        <div class="main__work-item" :class="{active: tabs === 'tab4'}">
          <div class="main__work-item__left">
            <img src="@/assets/img/plant-shop-work.png" alt="" />
          </div>
          <div class="main__work-item__right">
            <h2 class="main__work-item__title">PLANT SHOP Layout</h2>
            <p class="main__work-item__text">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Orci,
              mauris neque, gravida amet diam cum nisl enim. Vestibulum, risus,
              maecenas et nisi lobortis malesuada vel. Neque, sem tellus sed a,
              enim egestas. Mi mi id amet, lorem vitae lectus risus diam nunc.
              Eget nunc eget lectus amet feugiat lobortis sit sit non eu. Nunc,
              mauris viverra quis sapien quam. Non parturient sed
            </p>
            <a href="https://davron28.github.io/Plant-Shop/" target="_blank" class="main__work-item__btn">Посетить сайт</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  
  export default {
    data() {
      return {
        tabs: "tab1"
      }
    }
  }

</script>

<style>
</style>