<template>
  <input
    class="checkbox"
    v-bind="$attrs"
    :checked="modelValue"
    @change="$emit('update:modelValue', $event.target.checked)"
  />
  <label v-if="label" class="checkbox-label">{{ label }}</label>
</template>
<script>
export default {
  props: {
    label: {
      type: String,
      default: '',
    },
    modelValue: {
      type: Boolean,
      default: false,
    },
  },
}
</script>
<style lang="scss" scoped>
.checkbox {
  margin-right: 0.5rem;
  vertical-align: middle;
}
.checkbox-label {
  font-size: 0.8rem;
  vertical-align: bottom;
  color: #fff;
}
</style>
