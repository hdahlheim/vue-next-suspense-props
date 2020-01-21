<template>
  <img src="./logo.png">
  <h1>Hello Vue 3!</h1>
  <button @click="inc">Clicked {{ count }} times.</button>
  <Suspense>
    <AsyncComp :int="count" />
  </Suspense>
  <Comp :int="count" />
</template>

<script>
import { ref } from 'vue'
import AsyncComp from './AsyncComp.vue'
import Comp from './Comp.vue'

export default {
  components:{
    AsyncComp,
    Comp
  },
  setup() {
    const count = ref(0)
    const inc = () => {
      count.value++
    }

    return {
      count,
      inc
    }
  }
}
</script>

<style scoped>
img {
  width: 200px;
}
h1 {
  font-family: Arial, Helvetica, sans-serif;
}
</style>
