<template>
    <div class="urna-teclado">

        <div class="teclado-nemerico">
            <div class="urna-numero-linha">
                <button v-on:click="adicionarNumero(1)">1</button>
                <button v-on:click="adicionarNumero(2)">2</button>
                <button v-on:click="adicionarNumero(3)">3</button>
            </div>
            <div class="urna-numero-linha">
                <button v-on:click="adicionarNumero(4)">4</button>
                <button v-on:click="adicionarNumero(5)">5</button>
                <button v-on:click="adicionarNumero(6)">6</button>
            </div>
            <div class="urna-numero-linha">
                <button v-on:click="adicionarNumero(7)">7</button>
                <button v-on:click="adicionarNumero(8)">8</button>
                <button v-on:click="adicionarNumero(9)">9</button>
            </div>
            <div class="urna-numero-linha">
                <button v-on:click="adicionarNumero(0)">0</button>
            </div>
        </div>

        <div class="teclado-acoes">
            <button class="btn-branco" v-on:click="branco()">BRANCO</button>
            <button class="btn-corrige" v-on:click="corrigir()" >CORRIGE</button>
            <button class="btn-confirma">CONFIRMA</button>

        </div>

    </div>

</template>

<script>

import '@/css/global.css';

export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Teclado',
    props: {
        adicionarNumero: Function,
        corrigir: Function,
        branco: Function
    }
}

</script>

<style>
    .urna-teclado {
        width: 40%;
        height: 100%;
        background-color: var(--box-teclado);
        border-radius: 5px;
        padding: 20px;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
    }

    .teclado-numerico {
        width: 100%;
    }

    .urna-numero-linha {
        display: flex;
        justify-content: space-around;
        margin-bottom: 20px;
    }

    .urna-numero-linha button {
        background-color: var(--box-botao-teclado);
        color: var(--cor-texto-claro);
        font-size: 30px;
        border-radius: 5px;
        width: 5rem;
        height: 4rem;
    }

    .teclado-acoes {
        width: 100%;
        display: flex;
        justify-content: space-between;
    }

    .teclado-acoes button {
        color: var(--cor-texto-escuro);
        border-radius: 5px;
        width: 32%;
        height: 50px;
        font-weight: bold;
    }

    .btn-branco {
        background-color: var(--botao-branco);
        font-size: 90%;
    }

    .btn-corrige {
        background-color: var(--botao-corrige);
        font-size: 95%;
    }

    .btn-confirma {
        background-color: var(--botao-confirma);
        font-size: 90%;
        padding-right: 25px;
    }

</style>
