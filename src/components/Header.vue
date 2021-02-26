<template>
  <div class="header">
    <img :src="require('@/assets/images/logo.jpg')" alt="logo-alunison" />
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>
<style lang="scss" scoped>
.header {
  top: 0;
  padding: 0.7%;
  position: fixed;
  width: 100%;
  background-color: white;
  z-index: 10000;
}
</style>
