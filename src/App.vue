<script setup>
import {ref} from 'vue'
let msg = "Hallo Dunia ";
let headName = "<h1>Nama Saya Alvin</h1>"
let hai = true
let barang = [
  {nama:'Gayung'},
  {nama:'Meja'}
]
let baca = ref("Hai Vue JS")

function balik(){
  baca.value =  baca.value.split('').reverse().join('') 
}

let pesan = ref("Hai Vue")
</script>

<template>
  <div>
    <span>{{ msg }}</span> <br>
    <span style="color:red">Ini Warna Merah</span> <br>
    <span v-html="headName"></span>
    
    <button v-bind:disabled="isButtonDisabled">Tombol</button><br>
    <p v-if="hai">Hallo</p>
    {{ msg.split('').reverse().join('')
}}

  </div>
  <li v-for=" brg in barang">
    {{ brg.nama }}
  </li>
  <p>{{ baca }}</p>
    <button v-on:click="balik">Tomboll</button><br>

  <p>{{ pesan }}</p>
  <input v-model="pesan">
</template>