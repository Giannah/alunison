<template>
  <input class="button" v-bind="$attrs" :value="modelValue" />
</template>
<script>
export default {
  props: {
    modelValue: {
      type: String,
      default: '',
    },
  },
}
</script>
<style lang="scss" scoped>
.button {
  border-radius: 10px;
  padding: 0.5rem;
  margin: 1rem;
}

.button:focus {
  outline-offset: 0.1rem;
  outline-color: #fff;
}
</style>
