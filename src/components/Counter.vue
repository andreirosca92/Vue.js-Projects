<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      this.count--;
    },
    reset() {
      this.count = 0;
    },
  },
};
</script>

<template>
  <p>You clicked me {{ count }} times.</p>
  <button @click="increment">+</button>
  <button @click="decrement">-</button>
  <button @click="reset">reset</button>
</template>
