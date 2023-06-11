<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <teleport to=".modals" v-if="showModal">
    <Modal theme="dark" @close="toggleModal">
      <template v-slot:links>
        <a href="#">sign up now</a>
        <a href="#">more info</a>
      </template>
      <h1>Sign up for Blog!</h1>
      <p>Best experience in the world on our blog.</p>
    </Modal>
  </teleport>
  <div v-if="showModalTwo">
    <Modal @close="toggleModalTwo">
      <h1>Sign up to the newsletter</h1>
      <p>For updates and promo codes!</p>
    </Modal>
  </div>
  <button @click="toggleModal">open modal one</button>
  <button @click="toggleModalTwo">open modal two</button>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  data() {
    return {
      title: "My first Vue App :)",
      header: "Sign up for Blog!",
      text: "Best experience in the world on our blog.",
      showModal: false,
      showModalTwo: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo;
    },
  },
  components: {
    Modal,
  },
};
</script>

<style>
#app,
.modals {
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
