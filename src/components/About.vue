<template>
  <section aria-labelledby="section-title">
    <h2 class="section-title">La conviction d'Aluni'son</h2>
    <div class="section-content">
      <p class="flex-item">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sit inventore obcaecati
        voluptatibus temporibus dolor tempora exercitationem quas quisquam quis, hic quod ab iure
        culpa incidunt qui eos facilis, omnis dolore! Lorem ipsum dolor sit amet consectetur
        adipisicing elit. Impedit delectus, quas sequi iusto deleniti est voluptatibus quia incidunt
        quibusdam quis nostrum unde architecto rerum quos, minus iure corporis minima deserunt.
      </p>

      <img :src="require('@/assets/images/elderly.png')" alt="" class="flex-item" />
    </div>
    <div class="section-end">
      <font-awesome-icon :icon="myIcon" class="icon" />
    </div>
  </section>
</template>
<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faChevronCircleDown } from '@fortawesome/free-solid-svg-icons'

export default {
  name: 'About',
  data() {
    return {
      myIcon: faChevronCircleDown,
      show: false,
    }
  },
  components: {
    FontAwesomeIcon,
  },
}
</script>

<style lang="scss" scoped>
section {
  height: 100vh;
  width: 100vw;
  .section-content {
    text-align: left;
    width: 100%;
    display: flex;
    flex: row nowrap;
    justify-content: space-around;
    align-content: space-between;
    align-items: center;
    margin-bottom: 1rem;
    .flex-item {
      max-width: 40%;
      margin: 2%;
    }
  }
  .section-end {
    margin-top: 12%;
    .icon {
      font-size: 4rem;
      color: #00bbbb;
    }
  }
}
</style>
