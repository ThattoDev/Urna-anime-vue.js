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
            <button>BRANCO</button>
            <button>CORRIGE</button>
            <button>CONFIRMA</button>

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
    }

</style>
