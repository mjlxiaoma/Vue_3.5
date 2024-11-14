<script setup lang="ts">
import { ref } from 'vue'
function processData(data: any, callback: Function) {
  console.log("Processing data...");
  setTimeout(() => {
    let processedData = data * 2;
    callback(processedData);
  }, 1000);
}
function displayResult(result: any) {
  console.log("Processed result: " + result);
}
processData(10, displayResult);
defineProps<{ msg: string }>()
const count = ref(0)
const msg = 'Hello Vue 3 + Vite!'
</script>

<template>
  <h1>{{ msg }}</h1>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank">create-vue</a>, the official Vue + Vite
    starter
  </p>
  <p>
    Learn more about IDE Support for Vue in the
    <a href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support" target="_blank">Vue Docs Scaling up Guide</a>.
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
