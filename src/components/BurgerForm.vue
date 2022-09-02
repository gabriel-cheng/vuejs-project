<script>
    export default {
        name: 'BurgerForm'
    }
</script>

<template>
    <div id="burger-form-main-container">
        <p>Componente de Mensagem</p>
        <div>
            <form action="" id="burger-form">
                <div class="input-container">
                    <label for="name">Nome do cliente:</label>
                    <input type="text" name="name" id="inputName" v-model="name" placeholder="Digite seu nome">
                </div>
                <div class="input-container">
                    <label for="pao">Escolha o pão:</label>
                    <select name="pao" id="pao" v-model="pao">
                        <option value="">Selecione o seu pão:</option>
                        <option value="integral">Integral</option>
                    </select>
                </div>
                <div class="input-container">
                    <label for="carne">Escolha a carne do seu Burger:</label>
                    <select name="carne" id="carne" v-model="carne">
                        <option value="">Selecione o tipo de carne</option>
                        <option value="maminha">Maminha</option>
                    </select>
                </div>
                <div class="input-container">
                    <label for="opcionais">Selecione os opcionais:</label>
                    <div class="checkbox-container">
                        <input type="checkbox" name="opcionais" v-model="opcionais" value="Salame">
                        <span>Salame</span>
                    </div>
                </div>
                <div class="input-container">
                    <input type="submit" class="submit-btn" value="Criar meu Burger">
                </div>
            </form>
        </div>
    </div>
</template>

<style scoped>
    #burger-form-main-container {
        width: 500px;
    }

    #burger-form {
        margin: 20px 0 40px 0;
        min-width: 280px;
        width: 100%;
    }

    .input-container label {
        font-size: 1.6rem;
        font-weight: 600;
    }

    .input-container label {
        border-left: 2px solid var(--color-3);
        display: block;
        margin: 0 0 8px 0;
        padding: 0 4px;
    }

    .input-container:not(:last-child) {
        margin: 0 0 25px 0;
    }

    #inputName {
        width: 100%;
        height: 30px;
        font-size: 1.6rem;
    }

    #inputName, select {
        outline: 0;
        border: 0;
        border-bottom: 1px solid rgb(138, 138, 138);
        width: 100%;
    }

    .checkbox-container span {
        font-size: 1.7rem;
        font-weight: 600;
    }

    input[type=checkbox] {
        margin: 0 5px 0 0;
    }

    .submit-btn {
        width: 100%;
        background-color: #000;
        color: var(--color-3);
        padding: 20px;
        border: 0;
        font-weight: 600;
        font-size: 1.4rem;
        cursor: pointer;
    }

    .submit-btn:hover {
        background-color: rgba(0, 0, 0, 0.849);
    }
</style>
