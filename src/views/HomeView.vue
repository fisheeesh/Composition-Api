<template>
  <div class="home">
    <h1>Home</h1>
    <p>Hello {{ name }}</p>
    <p>I am {{ age }} years old.</p>

    <input type="text" v-model="name">
    <button @click="handleClick">Click</button>
    <button @click="age++">Increase Age</button>
  </div>
</template>

<script>
import { ref } from 'vue';


export default {
  setup(){
    /**
     * no reactive code
     */
    // let name = "Swan Yi Phyo"

    /**
     * reactive code
     */
    let name  = ref("Swan Yi Phyo")
    console.log(name.value)
    let age = ref(22)
    let handleClick = () => name.value = "Fisheeesh"
    return{ name, age, handleClick }
  }
}
</script>
