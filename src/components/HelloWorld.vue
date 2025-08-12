<script setup lang="ts">
import { ref } from 'vue'
import { useMotion } from "@vueuse/motion"

defineProps<{ msg: string }>()

const box = ref(null)

useMotion(box, {
  initial: { scale: 0.5, rotate: 0 },
  hover: { scale: 1.2, rotate: 15 },
  press: { scale: 0.9 },
})
</script>

<template>
  <h1>{{ msg }}</h1>
  <div ref="box" class="box">Hover Me</div>
  <div class="card">
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Learn more about IDE Support for Vue in the
    <a
      href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support"
      target="_blank"
      >Vue Docs Scaling up Guide</a
    >.
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.box {
  width: 100px;
  height: 100px;
  background: #42b983;
  border-radius: 8px;
  display: grid;
  place-items: center;
  cursor: pointer;
}
.read-the-docs {
  color: #888;
}
</style>
