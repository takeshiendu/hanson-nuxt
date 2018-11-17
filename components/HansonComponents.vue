<template lang="html">
  <div class="sample">
    <h1>{{ title }}</h1>
    <p>Hello, I'm {{ name }}</p>
    <!-- <div>
      <button
        type="button"
        name="button"
        @click="plus">click times: {{ num }}</button>
    </div>
    <div :class="['hide', { seven: num === 7 }]">
      click 7 times
    </div> -->
    <div class="slot">
      <slot/>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Default Title'
    }
  },
  data() {
    return {
      name: 'entak8'
    }
  },
  mounted() {
    console.log('mounted')
  },
  methods: {
    plus() {
      this.num++
    }
  }
}
</script>

<style lang="scss" scoped>
.hide {
  display: none;
  &.seven {
    display: block;
  }
}
.come {
  color: red;
}
</style>
