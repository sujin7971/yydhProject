<template>
  <div>
    <canvas
      ref="canvas"
      style="border: solid 1px #ccc;"
    ></canvas>

    <div
      ref="div"
      :style="{
        width: '100px',
        height: '100px',
        backgroundColor: color
      }"
    ></div>

    <test
      :name="name"
      @change="onChange"
    />

    <nuxt-link to="sign-in">이동</nuxt-link>
  </div>
</template>

<script>
import Test from '@/components/test'

export default {
  name: 'asdf',
  data() {
    return {
      name: '정재성',

      color: 'red'
    }
  },
  components: {
    Test
  },
  computed: {
  },
  methods: {
    onChange(name) {
      this.name = name;
    },
    move() {
      // this.$router.push('/sign-in')
    }
  },
  created() {
    // console.log(this.$axios.$get(''))
  },
  mounted() {
    console.log(this.$refs.canvas)
  },
  destroyed() {
  }
}
</script>

<style scoped>
</style>