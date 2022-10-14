<template>
    <div class="urna-tela">
        <div v-if="tela != 'fim'" class="urna-tela-voto">
            votação
        </div>
        <div v-if="tela == 'fim'"  class="urna-tela-fim">
            finalização
        </div>
    </div>
</template>

<script>
import '@/css/global.css';

export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Tela',
    props:{
        tela: String
    }
}
</script>

<style>

    .urna-tela {
        width: 100%;
        height: 100%;
        background-color: var(--box-tela);
        border-radius: 5px;
        border: 2px solid var(--borda-clara);
        padding: 20px;
        color: var(--cor-texto-escuro);
    }

</style>