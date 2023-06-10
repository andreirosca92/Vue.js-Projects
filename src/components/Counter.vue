<script>
export default {
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    increment() {
      this.counter++;
    },
    decrement() {
      if (this.counter > 0) this.counter--;
    },
    reset() {
      this.counter = 0;
    },
  },
};
</script>

<template>
  <p>You clicked me {{ counter }} times.</p>
  <button @click="increment">+</button>
  <button @click="decrement">-</button>
  <button @click="reset">reset</button>
</template>
