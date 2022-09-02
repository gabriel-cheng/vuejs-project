<script>
    export default {
        name: 'Navbar',
        props: ["logo", "alt"]
    }
</script>

<template>
    <nav id="main-navbar">
        <rounter-link to="/">
            <img :src="logo" :alt="alt" id="logo">
        </rounter-link>
        <div class="navigations-container">
            <router-link to="/">Home</router-link>
            <router-link to="/pedidos">Pedidos</router-link>
        </div>
    </nav>
</template>

<style scoped>
    #main-navbar {
        background-color: var(--color-3);
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 20px 25px;
        position: fixed;
        top: 0;
    }

    #logo {
        width: 60px;
    }

    .navigations-container a {
        font-size: 1.8rem;
        text-transform: uppercase;
        color: var(--color-1);
        padding: 15px;
        transition: 0.1s ease-in-out;
    }

    .navigations-container a:hover {
        background-color: red;
        color: #fff;
        transition: 0.1s ease-in-out;
    }
</style>
