<template>
  <div id="app">
    <div class="urna">
      
      <Tela
      :tela= "tela"
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
      tela: 'prefeito'
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
  gap: 15px;
}
</style>
