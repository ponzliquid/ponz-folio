<template>
  <div id="app">
    <!-- <div class="overpanel">
      <ponzheader></ponzheader>
    </div> -->

    <router-view></router-view>

    <div id="modals">
      <component v-for="(modal) in modals" :is="modal.component"  :key="modal.id" :params="modal.params"></component>
    </div>

    <div class="ft">
      <ponzfooter></ponzfooter>
    </div>

  </div>
</template>

<script>
import Vue from 'vue'
// import ponzheader from './components/ponzheader'
import ponzfooter from './components/ponzfooter'
import ModalAlert from './components/Modal/Alert'
import store from './components/store/'

Vue.component('modalAlert', ModalAlert)

export default {
  name: 'App',
  components: {
    // ponzheader,
    ponzfooter,
    ModalAlert
  },
  computed: {
    modals: () => {
      return store.getters.modals
    }
  }
}
</script>

<style>
body{
  background-color: #272727;
  color: #EFF1F3;
}
#app {
  font-family: 'Avenir', Verdana, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #EFF1F3;

  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.overpanel {
    position: sticky;
    opacity: 0.9;
    z-index: 100;
}
.ft {
  margin-left: -5px;
  margin-top: auto;
  opacity: 0.9;
}
</style>
