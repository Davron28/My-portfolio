  <template>
  <Transition name="header__modal">
    <div class="header__modal" @click="closeModal">
      <div class="header__modal-block" @click.stop="">
          <h2 class="header__modal-title">Заказ проекта</h2>
          <p class="header__modal-text">Заказать вёрстку сайта можно, связавшись со мной по ниже указанным соц.сетям . <br> <span>(o˘◡˘o)</span></p>
          <ul class="header__modal-list">
              <li><a href="https://www.facebook.com/profile.php?id=100021213317431" class="header__modal-link" target="_blank"><span class="icon__facebook"></span></a></li>
              <li><a href="https://www.instagram.com/nklaugh28/" class="header__modal-link" target="_blank"><span class="icon__instagram"></span></a></li>
              <li><a href="https://t.me/NkLaugh" class="header__modal-link" target="_blank"><span class="icon__telegram"></span></a></li>
          </ul>
          <button class="header__modal-btn" @click="closeModal"><span class="icon__close"></span></button>
      </div>
    </div>
  </Transition>
</template>

<script>
export default {
  props: {
    openModal: Boolean
  },
  methods: {
    closeModal() {
      this.$emit('closeModal', false)
    }
  }
}
</script>

<style>

</style>