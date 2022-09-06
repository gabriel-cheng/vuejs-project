<script>
    import Dashboard from '../components/Dashboard.vue';

    export default {
        name: "Pedidos",
    components: {
        Dashboard
    }
}
</script>

<template>
    <div id="main-container">
        <div class="content">
            <h1>Gerenciar pedidos: </h1>
            <Dashboard />
        </div>
    </div>
</template>

<style scoped>
    #main-container {
        margin: 110px 0 0 0;
    }

    .content h1 {
        font-size: 5rem;
        text-align: center;
        margin: 0 0 90px 0;
    }
</style>
