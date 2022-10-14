<template>
    <div class="urna-teclado">

        <div class="teclado-nemerico">
            <div class="urna-numero-linha">
                <button>1</button>
                <button>2</button>
                <button>3</button>
            </div>
            <div class="urna-numero-linha">
                <button>4</button>
                <button>5</button>
                <button>6</button>
            </div>
            <div class="urna-numero-linha">
                <button>7</button>
                <button>8</button>
                <button>9</button>
            </div>
            <div class="urna-numero-linha">
                <button>0</button>
            </div>
        </div>

        <div class="teclado-acoes">
            <button class="btn-branco">BRANCO</button>
            <button class="btn-corrige">CORRIGE</button>
            <button class="btn-confirma">CONFIRMA</button>

        </div>

    </div>

</template>

<script>

import '@/css/global.css';

export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Teclado'
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
        font-size: 18px;
        border-radius: 5px;
        width: 32%;
        height: 50px;
    }

    .btn-branco {
        background-color: var(--botao-branco);
    }

    .btn-corrige {
        background-color: var(--botao-corrige);
    }

    .btn-confirma {
        background-color: var(--botao-confirma);
    }

</style>
