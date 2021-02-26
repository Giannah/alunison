<template>
  <form action="">
    <button @click="$emit('unclicked')">Retour</button>
    <h3 class="section-subtitle">Testez Aluni'son en avant-première</h3>
    <BasicInput v-model="lastname" label="Nom" type="text" />
    <BasicInput v-model="firstname" label="Prénom" type="text" />
    <BasicInput v-model="email" label="Email" type="email" />
    <div>
      <BasicCheckbox type="checkbox" v-model="checked" :label="textConsent" />
    </div>
    <div class="form-control">
      <BasicButton class="button" type="submit" value="Envoyer" />
      <BasicButton class="button" type="reset" value="Annuler" />
    </div>
  </form>
</template>
<script>
import BasicInput from '@/components/BasicInput.vue'
import BasicButton from '@/components/BasicButton.vue'
import BasicCheckbox from '@/components/BasicCheckbox.vue'
import consent from '@/content/consent.json'
export default {
  name: 'Form',
  components: {
    BasicInput,
    BasicButton,
    BasicCheckbox,
  },
  data() {
    return {
      lastname: '',
      firstname: '',
      email: '',
      textConsent: '',
      checked: false,
    }
  },
  created() {
    this.textConsent = consent.textConsent
  },
  emits: ['clicked'],
}
</script>
<style lang="scss" scoped>
form {
  width: 40%;
  text-align: center;
  margin-top: 3%;
  margin-right: 10%;
  margin-left: 25%;
  padding: 2%;
  border-radius: 10px;
  background-color: transparentize($color: #000000, $amount: 0.9);

  .form-control {
    display: flex;
    flex: row nowrap;
    align-items: center;
    margin-left: 30%;
    .button {
      color: #fff;
      font-weight: bold;
    }
    input[type='submit'] {
      background-color: #00bbbb;
      border-color: #00bbbb;
    }
    input[type='reset'] {
      background-color: #ffc254;
      border-color: #ffc254;
    }
  }
}

@media screen and (min-width: 200px) and (max-width: 812px) {
  form {
    margin: 0;
    width: 100%;
    height: 30%;
  }
}
</style>
