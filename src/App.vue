<script>
    import Navbar from './components/Navbar.vue';
    import Footer from './components/Footer.vue';

    export default {
        components: {
            Navbar,
            Footer
        },
        data() {
            return {
                logo_src: "/img/logo.png",
                app_name: "/img/make-your-burger.png"
            }
        }
    }
</script>

<template>
    <Navbar :logo="logo_src" :alt="app_name" />
    <router-view/>
    <Footer />
</template>

<style>
    :root {
        --color-1: #D90404;
        --color-2: #579707;
        --color-3: #F28705;
        --color-4: #F29F05;
    }

    * {
        padding: 0;
        margin: 0;
        box-sizing: border-box;
        font-family: Helvetica;
    }

    html, body {
        width: 100%;
        height: 100vh;
    }

    html {
        font-size: 62.5%;
    }

    a {
        text-decoration: none;
    }

    #main-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
</style>
