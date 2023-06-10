<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <div v-if="showModal">
    <ModalVue theme="dark" @close="toggleModal">
      <template v-slot:links>
        <a href="#">sign up now</a>
        <a href="#">more info</a>
      </template>
      <h1>"Sign up for Blog!"</h1>
      <p>"Best experience in the world on our blog."</p>
    </ModalVue>
  </div>
  <button @click="toggleModal">open modal</button>
</template>

<script>
import ModalVue from "./components/Modal.vue";

export default {
  name: "App",
  data() {
    return {
      title: "My first Vue App :)",
      header: "Sign up for Blog!",
      text: "Best experience in the world on our blog.",
      showModal: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
  },
  components: {
    ModalVue,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  border-bottom: 1px solid #ddd;
  display: inline block;
  padding-bottom: 10px;
}
</style>
