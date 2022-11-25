<script setup>

import {sayHello} from "../api/hello.js";
import {ref} from "vue";

let msg = ref('Yili Music Admin')
const hi = () =>{
  sayHello().then(res=>{
    msg.value = res.data;
  })
}


</script>

<template>
  <h1>{{ msg }}</h1>

  <q-btn @click="hi" color="secondary" label="Welcome" />
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
