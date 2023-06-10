<template>
  <div class="backdrop">
    <div class="modal" :class="{ dark: theme === 'dark' }">
      <h1>{{ header }}</h1>
      <p>{{ text }}</p>
    </div>
  </div>
</template>
<script>
export default {
  props: ["header", "text", "theme"],
};
</script>

<style>
.modal {
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background: white;
  border-radius: 10px;
}
.backdrop {
  top: 0;
  position: fixed;
  background: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
}
.modal h1 {
  color: #03cfb4;
  border: none;
  padding: 0;
}
.modal p {
  font-style: normal;
}
.modal.dark {
  background: rgb(69, 67, 67);
  color: white;
}
.modal.dark h1 {
  color: white;
}
</style>
