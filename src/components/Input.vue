<template>
  <div class="input-wrapper">
    <input class="input" @input="onInput" :placeholder="placeholder" :type="type">
  </div>
</template>

<script>
export default {
  name: 'chat-input',
  props: {
    type: {
      type: String,
      default: 'text'
    },
    placeholder: String
  },
  methods: {
    onInput(e) {
      this.$emit('input', e.target.value)
    }
  }
}
</script>
