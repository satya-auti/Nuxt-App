<template>
    <div>
        <h1 class="bg-black rounded-xl text-teal-700"> Hello I'm Nuxt-Demo</h1>
    </div>
    <inner-nuxt />

    <!-- </inner-nuxt> -->
</template>

<script>
import InnerNuxt from '~/components/inner-nuxt.vue';

definePageMeta({
    components: { 
        InnerNuxt 
    }
})

</script>

<style scoped>

</style>
