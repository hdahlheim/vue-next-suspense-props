<template>
  <div>
    Not Async Comp {{ int }}
  </div>
</template>

<script>
import { ref, watch } from 'vue'
export default {
  props:{
    int: Number
  },
  setup(props){
    watch(() => {
      console.log('Not Async Comp'  + props.int)
    })
    return
  }
}
</script>
