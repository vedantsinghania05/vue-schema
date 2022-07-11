<script setup>

import { ref } from 'vue'
import json from './data.json'

const data = ref(json)

</script>



<template>
<div v-for='item in data'>
  <p>{{item.title}}</p>
  <p>{{item.messageTitle}}: {{item.message}}</p>

  <input :type="item.type" :id="item.type" v-model="item.message" :placeholder="item.placeholder">
  <label v-if="item.label != null">{{item.label}}</label>
  <br>
  <br>

</div>

</template>
