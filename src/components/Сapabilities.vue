<template>
    <h2 class="main__capabilities-title">Навыки</h2>
    <div class="main__capabilities" data-aos="fade-up"
     data-aos-anchor-placement="bottom-bottom">
        <div class="container capabilities">
            <div class="main__capabilities-left">
                <Accordion/>
            </div>
            <div class="main__capabilities-right">
                <img src="@/assets/img/main-human.png" alt="">
            </div>
        </div>
    </div>
</template>

<script>

import Accordion from "@/components/Accordion.vue"
export default {
    components: {
        Accordion
    },
}
</script>

<style>

</style>