<template>
  <div id="app">
    <div class="urna">
      
      <Teclado/>

    </div>
  </div>
</template>

<script>

import '@/css/global.css';

import Teclado from '@/components/teclado.vue';

export default {
  name: 'App',
  components: {
    Teclado
    
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
  width: 70%;
  height: 70%;
  background-color: var(--bg-box);
  padding: 30px;
  border-radius: 10px;
  display: flex;
}
</style>
