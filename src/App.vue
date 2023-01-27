<template>
  <div id="app">
    <div class="urna">
      
      <Tela
      :tela= "tela"
      :numeroVoto= "numeroVoto"
      :quantidadeNumeros= "quantidadeNumeros"
      :candidato= "candidato"
      />
      <Teclado
      :adicionarNumero="adicionarNumero"
      :corrigir="corrigir"
      :branco="branco"
      :confirma="confirma"
      />

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
  methods: {
    adicionarNumero(numero) {
      if(this.numeroVoto.length == this.quantidadeNumeros)
      return false

      this.numeroVoto += ''+numero;
    
      this.verificarCandidato();
    },

    verificarCandidato() {
      if(this.numeroVoto.length < this.quantidadeNumeros)
      return false

      if(this.candidatos[this.tela][this.numeroVoto]) {
        this.candidato = this.candidatos[this.tela][this.numeroVoto];
        return true
      }
      
      this.candidato = {
        nome: 'voto nulo',
        partido: 'voto nulo',
        imagem: ''
      }

    },

    limpar() {
      this.candidato = {}
      this.numeroVoto = ''
    },

    corrigir() {
      this.limpar();
    },


    branco(){
      this.limpar();
      this.candidato= {nome: 'voto em branco',
      partido: 'voto em branco',
      imagem: ''}
    },

    confirma(){
      this.limpar();
      this.tela = 'vereador';
    }
  },
  data() {
    return {
      tela: 'prefeito',
      numeroVoto: '',
      quantidadeNumeros: 2,
      candidato:{},
      candidatos: {
        "prefeito": {
          "21":{
            "nome": "Toji",
            "partido": "Jujutsu",
            "imagem": './assets/images/Maki-prefeita.jpg'
          },
           "27":{
            "nome": "Maki",
            "partido": "Jujutsu0",
            "imagem": <img src="./assets/images/Maki-prefeita.jpg"/>
          },
           "23":{
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
