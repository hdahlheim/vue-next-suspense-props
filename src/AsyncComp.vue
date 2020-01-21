<template>
  <div>
    Async Comp {{ int }}
  </div>
</template>

<script>
import { ref, watch } from 'vue'
export default {
  props:{
    int: Number
  },
  async setup(props){
    watch(() => {
      console.log('Async Comp'  + props.int)
    })
    return
  }
}
</script>
