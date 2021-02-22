<template>
  <div class="first-section">
    <h1>Bienvenue chez Aluni'son!</h1>
    <section aria-labelledby="section-title">
      <h2 class="section-title">Participez à l'aventure!</h2>
      <Form />
    </section>
  </div>
</template>
<script>
import Form from '@/components/Form.vue'

export default {
  components: {
    Form,
  },
}
</script>
<style lang="scss" scoped>
.first-section {
  padding: 1rem;
  height: 90vh;
  background-image: url('../assets/images/bg2.jpg');
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
