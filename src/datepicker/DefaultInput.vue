<template>
  <input type="text" readonly="readonly" :value="date" @click='showPicker'/>
</template>

<script lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
  props: {
    date: {
      type: String,
      required: true
    },
    disabled: {
      type: Boolean,
      required: true
    },
    placeholder: {
      type: String
    }
  },
  setup(props, { emit }) {

    const showPicker = () => {
      emit('click')
    }

    return {
      showPicker
    }
  }
})
</script>

<style scoped>

</style>