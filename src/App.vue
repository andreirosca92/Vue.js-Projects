<template>
  <h1>My first {{ title }}</h1>
  <br />
  <ModalVue :header="header" :text="text" theme="dark" />
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
    };
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
