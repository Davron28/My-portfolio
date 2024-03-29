<template>
  <main class="main">
    <img src="@/assets/img/main-bg.png" alt="" class="main__top">
    <Human/>
    <Capabilities/>
    <TabLink/>
    <img src="@/assets/img/main-bg-2.png" alt="" class="main__bottom">
  </main>
</template>

<script>
import Human from "@/components/Human.vue"
import Capabilities from "@/components/Сapabilities.vue"
import TabLink from "@/components/TabLink.vue"

export default {
 components: {
   Human,
   Capabilities,
   TabLink
 }
}
</script>

<style>

</style>