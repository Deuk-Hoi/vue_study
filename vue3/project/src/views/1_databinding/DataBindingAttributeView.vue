<template>
  <div>
    <input type="text" v-bind:value="userId" readonly />
    <input type="text" :value="userId" readonly />
    <br />
    <img :src="imgSrc" style="width: 100px; height: auto" />
    <br />
    <input type="search" v-model="txt1" />
    <button :disabled="txt1 === ''">조회</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: 'asdsad',
      imgSrc: 'https://upload.wikimedia.org/wikipedia/commons/f/f1/Vue.png',
      txt1: ''
    }
  },
  setup() {},
  create() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
