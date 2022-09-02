<script>
    export default {
        name: "Banner"
    }
</script>

<template>
    <div id="main-banner">
        <h1>Make your Burger</h1>
    </div>
</template>

<style scoped>
    #main-banner {
        background-image: url('/public/img/burger.jpg');
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        height: 500px;
        display: flex;
        align-items: center;
        justify-content: flex-start;
        margin: 100px 0 0 0;
    }

    #main-banner h1 {
        font-size: 5rem;
        color: var(--color-4);
        margin: 0 0 0 40px;
    }
</style>
