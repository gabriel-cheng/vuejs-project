<script>
import { thisExpression } from '@babel/types';

    export default {
        name: 'Dashboard',
        data() {
            return {
                burgers: null,
                burger_id: null,
                status: []
            }
        },
        methods: {
            async getPedidos() {
                const request = await fetch('http://localhost:3000/burgers');

                const data = await request.json();

                this.burgers = data;

                this.getStatus();
            },
            async getStatus() {
                const request = await fetch('http://localhost:3000/status');

                const data = await request.json();

                this.status = data;

                console.log(data);
            }
        },
        mounted() {
            this.getPedidos();
        }
    }
</script>

<template>
    <div id="burger-table">
        <div>
            <div id="burger-table-heading">
                <div class="order-id">#:</div>
                <div>Cliente:</div>
                <div>Pão:</div>
                <div>Carne:</div>
                <div>Opcionais:</div>
                <div>Ações:</div>
            </div>
        </div>
        <div id="burger-table-rows">
            <div class="burger-table-row" v-for="burger in burgers" :key="burger.id">
                <div class="order-number">{{ burger.id }}</div>
                <div>{{ burger.nome }}</div>
                <div>{{ burger.pao }}</div>
                <div>{{ burger.carne }}</div>
                <div>
                    <ul>
                        <li v-for="(opcionais, index) in burger.opcionais" :key="index">{{ opcionais }}</li>
                    </ul>
                </div>
                <div class="status-container">
                    <select name="status" class="status">
                        <option v-for="item in status" :key="item.id" value="item.tipo" :selected="burger.status == item.tipo">{{ item.tipo }}</option>
                    </select>
                    <button class="delete-btn">Cancelar</button>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
    #burger-table {
        max-width: 1200px;
        margin: 0 auto;
        font-size: 1.6rem;
    }

    #burger-table-heading,
    #burger-table-rows,
    .burger-table-row {
        display: flex;
        flex-wrap: wrap;
    }

    #burger-table-heading {
        font-weight: bold;
        padding: 12px;
        border-bottom: 3px solid #333;
    }

    .burger-table-row {
        width: 100%;
        padding: 12px;
        border-bottom: 1px solid #CCC;
    }

    #burger-table-heading div,
    .burger-table-row div {
        width: 19%;
    }

    #burger-table-heading .order-id,
    .burger-table-row .order-number {
        width: 5%;
    }

    .status-container {
        display: flex;
    }

    select {
        padding: 12px 6px;
        margin-right: 12px;
        height: 40px;
    }

    .delete-btn {
        background-color: #222;
        color:#fcba03;
        font-weight: bold;
        border: 2px solid #222;
        padding: 10px;
        font-size: 16px;
        margin: 0 auto;
        cursor: pointer;
        transition: .5s;
        height: 40px;
    }

    .delete-btn:hover {
        background-color: transparent;
        color: #222;
    }
  </style>
