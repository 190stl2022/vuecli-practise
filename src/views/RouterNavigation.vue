<template>
  <button type="button" @click="getRute">getRoute</button>
  <button type="button" @click="push">Push</button>
  <button type="button" @click="replace">Replace</button>
  <button type="button" @click="go">Go</button>
  <hr>
  <button type="button" @click="addRoute">新增路由</button>
</template>

<script>
export default {
  methods: {
    push () {
    },
    getRute () {
      console.log(this.$route)
    },
    replace () {},
    go () {},
    addRoute () {}
  }
}
</script>
