<template>
 <div id="app">
  <button id="show-modal" @click="showModal = true"> 
    Show Modal
  </button>
  <modal v-if="showModal" @close="showModal = false">
    <h3 slot="header">Hey There!</h3>
  </modal>
 </div>
</template>

<script>
import modal from './components/modal.vue';

export default {
  name: "app",
  components: {
    modal,
  },

  data() {
    return {
      showModal: false,
    };
  }

}
</script>

<style>
 h3 {
   color: #4AAE9B;
 }
 #show-modal {
   background: #4AAE9B;
    color: white;
    border-radius: 3px;
 }
</style>
