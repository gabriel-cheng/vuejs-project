<script>
    export default {
        name: 'Footer'
    }
</script>

<template>
    <footer id="footer-container">
        <section class="footer-section-1">
            <p>Make your Burger &copy; 2022</p>
        </section>
        <section class="footer-section-2">
            <p>Todos os direitor reservados &copy; • Gabriel Carvalho</p>
        </section>
    </footer>
</template>

<style scoped>
    #footer-container {
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        background-color: var(--color-1);
        width: 100%;
        height: 40px;
    }

    #footer-container p {
        font-size: 1.4rem;
    }

    .footer-section-1 {
        display: flex;
        align-items: center;
        justify-content: flex-end;
        padding: 0 30px;
    }

    .footer-section-1 p {
        color: #fff;
    }

    .footer-section-2 {
        display: flex;
        justify-content: center;
        background-color: var(--color-2);
        margin: 4px 0 0 0;
    }

    .footer-section-2 p {
        margin: 0;
        color: #000;
    }
</style>
