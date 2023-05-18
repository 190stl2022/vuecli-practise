<template>
  <div class="container-xl">
    <div class="home text-center">
      <img alt="Vue logo" src="../assets/logo.png">
      <HelloWorld msg="Welcome to Your Vue.js App"/>
    </div>
    <v-form @submit="onSubmit" v-slot="{ errors}">
      {{ errors }}
      <div class="mb-3">
        <label for="email" class="form-label">Email</label>
        <v-field id="email" name="email" type="email" class="form-control" rules="email|required" :class="{ 'is-invalid': errors['email'] }" v-model="user.email"
                 placeholder="請輸入 Email"></v-field>
        <error-message name="email" class="invalid-feedback"></error-message>
      </div>
      <div class="mb-3">
        <label for="name" class="form-label">姓名</label>
        <v-field id="name" name="姓名" type="text" class="form-control" rules="required" :class="{ 'is-invalid': errors['姓名'] }" v-model="user.name"
                 placeholder="請輸入姓名"></v-field>
        <error-message name="姓名" class="invalid-feedback"></error-message>
      </div>
      <div class="mb-3">
        <label for="phone" class="form-label">電話</label>
        <v-field id="phone" name="電話" type="text" class="form-control" :rules="isPhone" :class="{ 'is-invalid': errors['電話'] }" v-model="user.phone"
                 placeholder="請輸入電話"></v-field>
        <error-message name="電話" class="invalid-feedback"></error-message>
      </div>
      <div class="mb-3">
        <label for="region" class="form-label">地區</label>
        <v-field as="select" id="region" name="地區" class="form-control" rules="required" :class="{ 'is-invalid': errors['地區'] }" v-model="user.area">
          <option value="" disabled>請選擇地區</option>
          <option value="台北市">台北市</option>
          <option value="高雄市">高雄市</option>
        </v-field>
        <error-message name="地區" class="invalid-feedback"></error-message>
      </div>
      <div class="mb-3">
        <label for="address" class="form-label">地址</label>
        <v-field id="address" name="地址" type="text" class="form-control" rules="required" :class="{ 'is-invalid': errors['地址'] }" v-model="user.address"
                 placeholder="請輸入地址"></v-field>
        <error-message name="地址" class="invalid-feedback"></error-message>
      </div>
      <button class="btn btn-primary" type="submit">Submit</button>
    </v-form>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  data () {
    return {
      user: {
        email: '',
        name: '',
        area: '',
        address: '',
        phone: ''
      }
    }
  },
  methods: {
    onSubmit () {
      console.log(this.user)
    },
    isPhone (value) {
      const phoneNumber = /^(09)[0-9]{8}$/
      return phoneNumber.test(value) ? true : '需要正確的電話號碼'
    }
  },
  created () {
    console.log(this)
  },
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
