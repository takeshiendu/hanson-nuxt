<template>
  <div>
    <hanson-components :title="indexTitle">
      <div class="come">
        slot example
      </div>
    </hanson-components>
    <nuxt-link to="/about">ABOUT</nuxt-link>
  </div>
</template>

<script>
import HansonComponents from '~/components/HansonComponents.vue'

export default {
  components: {
    HansonComponents
  },
  data() {
    return {
      indexTitle: 'Nuxt.js HansOn'
    }
  }
}
</script>

<style>
</style>
