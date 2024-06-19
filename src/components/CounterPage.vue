<template>
  <div>
    <p>
      The count is: <span>{{ count }}</span>
    </p>
    <button class="dec" @click="dec">-</button>
    <button class="inc" @click="inc">+</button>
  </div>
</template>

<script setup>
import { ref } from "vue";
const count = ref(0);
function inc() {
  count.value++;
}
function dec() {
  if (count.value > 0) {
    count.value--;
  }
}
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  list-style: none;
  text-decoration: none;
}

div {
  vertical-align: top;
}
button {
  margin: 0 15px;
  border: 0.5px rgb(0, 0, 0) solid;
  width: 100px;
  height: 60px;
  font-size: 50px;
  border-radius: 16px;
  background-color: rgb(255, 255, 255);
  transition: 500ms ease-in-out all;
  cursor: pointer;
}
button:hover {
  background-color: rgb(204, 203, 238);
}
.inc:focus {
  color: green;
}
.inc:not(:hover) {
  color: black;
}
.dec:focus {
  color: rgb(148, 50, 50);
}
.dec:not(:hover) {
  color: black;
}
p {
  border-radius: 10px;
  vertical-align: top;
  text-align: center;
  font-size: 30px;
  margin: 20px 0;
}
span {
  font-size: 35px;
  font-weight: 600;
}
</style>
