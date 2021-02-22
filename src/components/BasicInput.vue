<template>
  <div class="field">
    <label v-if="label">{{ label }}</label>
    <input
      v-bind="$attrs"
      :placeholder="label"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
    />
  </div>
</template>
<script>
export default {
  props: {
    label: {
      type: String,
      default: '',
    },
    modelValue: {
      type: String,
      default: '',
    },
  },
}
</script>
<style lang="scss" scoped>
.field {
  width: 80%;
  margin: 0.5rem;
  padding: 0.5rem;
}
label {
  color: #fff;
  width: 10%;
  text-align: left;
  font-weight: bold;
  font-size: 1.2rem;
  display: block;
  margin-left: 12rem;
  margin-right: 1.5rem;
  padding: 0.5rem;
}
input {
  width: 40%;
  border-color: #fff;
  border-radius: 10px;
  padding: 0.5rem;
  background-color: transparent;
  margin-left: 4.5rem;
}
input:focus {
  outline-color: #fff;
}
input::placeholder {
  color: #fff;
  font-style: italic;
  font-size: 0.8rem;
}
</style>
