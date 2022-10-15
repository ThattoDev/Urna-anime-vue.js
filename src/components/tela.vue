<template>
    <div class="urna-tela">
        <div v-if="tela != 'fim'" class="urna-tela-voto">
            <div class="urna-tela-voto-textos">
                <div class="urna-tela-voto-titulo">Seu voto para</div>
                <div class="urna-tela-voto-tipo"> {{tela}}</div>
                <div class="urna-tela-voto-numeros">

                    <div class="urna-tela-voto-numero" v-for="{value,key} in numeroVoto.padEnd(quantidadeNumeros,' ')" :key="key">
                        {{value}}
                    </div>

                </div>
            </div>
            <div class="urna-tela-voto-imgs">

            </div>
            <div class="urna-tela-voto-instrucoes">

            </div>
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
        tela: String,
        numeroVoto: String,
        quantidadeNumeros: Number

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

    .urna-tela-voto-titulo {
        font-size: 20px;
    }

    .urna-tela-voto-tipo {
        font-size: 30px;
        font-weight: bold;
        margin: 20px 0;
        text-transform: uppercase;
    }

    .urna-tela-voto-numeros {
        display: flex;
    }

    .urna-tela-voto-numero {
        width: 45px;
        height: 55px;
        color: red;
        border: 1px solid var(--borda-escura);
        align-items: center;
        margin-left: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 30px;
    }


</style>