<template>
  <div class="first-section">
    <section aria-labelledby="section-title">
      <div v-show="!isClicked">
        <div class="greet">
          <h1>Rejoignez l'aventure !</h1>
          <button class="participate" @click="isClicked = true">J'y vais</button>
        </div>
      </div>
      <transition
        name="custom-classes-transition"
        enter-active-class="animate__animated animate__flipInY"
        leave-active-class="animate__animated animate__flipOutY"
        mode="out-in"
      >
        <div v-if="isClicked" @unclicked="isClicked = false">
          <Form />
        </div>
      </transition>
    </section>
  </div>
</template>
<script>
import Form from '@/components/Form.vue'

export default {
  components: {
    Form,
  },
  data() {
    return {
      isClicked: false,
    }
  },
  methods: {
    changeClickState() {},
  },
}
</script>
<style lang="scss" scoped>
.first-section {
  padding: 0.5%;
  height: 100vh;
  width: 100vw;
  background-image: url('../assets/images/bg2.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: right 35% bottom 35%;
  .greet {
    margin-top: 15%;
    .participate {
      font-weight: bold;
      color: #00bbbb;
      background-color: #fff;
      border-color: #fff;
      border-radius: 10px;
      padding: 0.5rem;
    }
  }
}
</style>
