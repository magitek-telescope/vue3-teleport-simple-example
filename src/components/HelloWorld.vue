<template>
  <div>
    <h1>Hello Vue 3.0 + Vite</h1>
    <button @click="toggleModal">
      Open modal
    </button>
    <p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
    <teleport to="#modal-container">
      <div class="modal" v-if="state.isOpenModal">
        <div class="modal-content">
          <h2>Modal</h2>
          <button type="button" @click="toggleModal">Close Modal</button>
        </div>
      </div>
    </teleport>
  </div>
</template>

<script lang="ts">
import { reactive } from 'vue'

export default {
  name: 'HelloWorld',
  setup() {
    const state = reactive({
      isOpenModal: false
    })
    const toggleModal = () => {
      state.isOpenModal = !state.isOpenModal
    }
    return {
      state,
      toggleModal
    }
  }
}
</script>

<style scoped>
.modal {
  position: fixed;
  left: 0;
  top: 0;
  width: 100vw;
  height: 100vh;
  background: rgba(0,0,0,0.4);
}
.modal-content {
  max-width: 400px;
  margin: 3rem auto;
  padding: 0.75rem 1.5rem 2.25rem;
  background: #fff;
  border-radius: 4px;
}
</style>
