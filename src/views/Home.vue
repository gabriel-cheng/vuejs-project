<script>
    import Banner from '../components/Banner.vue';
    import BurgerForm from '@/components/BurgerForm.vue';

    export default {
        name: 'Home',
        components: {
            Banner,
            BurgerForm
        }
    }
</script>

<template>
    <Banner />
    <div id="main-container">
        <div class="content">
            <h1>Monte seu burger</h1>
        </div>
        <BurgerForm />
    </div>
</template>

<style scoped>
    .content h1 {
        font-size: 3.5rem;
        margin: 0 0 50px 0;
    }
</style>
