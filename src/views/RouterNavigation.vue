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
      this.$router.push({
        name: 'about'
      })
    },
    getRute () {
      console.log(this.$router)
    },
    replace () {
      this.$router.replace({
        name: 'about'
      })
    },
    go () {
      this.$router.go(-1)
    },
    addRoute () {
      this.$router.addRoute({
        path: '/newAbout',
        name: 'newAbout',
        component: () => import('./AboutView.vue')
      })
    }
  }
}
</script>
