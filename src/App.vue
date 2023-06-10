<template>
  <Navbar />
  <h1>My first {{ title }}</h1>
  <Counter />
  <Footer />
</template>

<script>
import Counter from "./components/Counter.vue";
import Footer from "./components/Footer.vue";
import Navbar from "./components/Navbar.vue";

export default {
  name: "App",
  data() {
    return {
      title: "My first Vue App :)",
    };
  },
  components: {
    Counter,
    Footer,
    Navbar,
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
