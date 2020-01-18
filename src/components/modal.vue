<template>
  <transition name="modal-trans">
      <div id="main-modal" class="modal-background">
            <div class="modal-container">
               <div class="modal-header">
                  <slot name="header">
                  Hey there!!
                  </slot>
               </div>

               <div class="modal-body">
                  <slot name="body">
                  Learn Vue in Three weeks
                  </slot>
               </div>

               <div class="modal-footer">
                  <slot name="footer">
                  Contact me now
                  <button class="modal-button" @click="$emit('close')">
                  Okay
                  </button>
                  </slot>
               </div>

            </div>
      </div>
   </transition>
</template>

<script>
 export default {
 name: "modal",
}
</script>
<style scoped>
 .modal-background {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(0, 0, 0, .5);
    transition: opacity .2s ease;
    display: flex;
    justify-content: center;
    align-items: center;
 }

 .modal-container {
    background-color: #ffffff;
    box-shadow: 2px 2px 20px 1px;
    display: flex;
    flex-direction: column;
    font-family: Helvetica, Arial, sans-serif;
    margin: 20px;
    padding: 20px;
 }

 .modal-header {
    display: flex;
    padding: 10px;
    justify-content: space-between;
 }

 .modal-body {
    position: relative;
   
 }

 .modal-footer {
    display: flex;
    padding: 10px;
    justify-content: space-between;
 }

 .modal-button {
    background: #4AAE9B;
    color: white;
    border-radius: 3px;
 }
</style>