<template>
  <div id="app">
    <div class="urna">
      
      <Tela
      :tela= "tela"
      :numeroVoto= "numeroVoto"
      :quantidadeNumeros= "quantidadeNumeros"
      />
      <Teclado/>

    </div>
  </div>
</template>

<script>

import '@/css/global.css';

import Teclado from '@/components/teclado.vue';
import Tela from '@/components/tela.vue';

export default {
  name: 'App',
  components: {
    Teclado,
    Tela
    
  },
  data() {
    return {
      tela: 'prefeito',
      numeroVoto: '',
      quantidadeNumeros: 2,
      candidato:{},
      candidatos: {
        "prefeito": {
          "11":{
            "nome": "Toji",
            "partido": "Jujutsu",
            "imagem": ''
          },
           "17":{
            "nome": "Maki",
            "partido": "Jujutsu0",
            "imagem": ''
          },
           "21":{
            "nome": "Naruto",
            "partido": "Konoha",
            "imagem": ''
          },
           "71":{
            "nome": "Gojo",
            "partido": "JujutsuFilme",
            "imagem": ''
          }
        },
        
        "vereador": {
           "111":{
            "nome": "Levi",
            "partido": "Shingeki",
            "imagem": ''
          },
           "171":{
            "nome": "Sasuke",
            "partido": "Konoha",
            "imagem": ''
          },
           "222":{
            "nome": "Nobara",
            "partido": "Jujutsu",
            "imagem": ''
          },
           "157":{
            "nome": "Sukuna",
            "partido": "Jujutsu0",
            "imagem": ''
          }

        }
      }
    }
  }
}
</script>

<style>
#app {
  
  background-color: var(--bg-page);
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;

}

.urna {
  width: 80%;
  height: 80%;
  background-color: var(--bg-box);
  padding: 20px;
  border-radius: 10px;
  display: flex;
  gap: 20px;
}
</style>
