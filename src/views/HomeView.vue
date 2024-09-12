<template>
  <div class="home">
    <h1>Home</h1>
    <p>Hello {{ name }}</p>
    <p>I am {{ age }} years old.</p>
    <button @click="handleClick">Click</button>
  </div>
</template>

<script>

export default {
  setup(){
    // console.log('hi there')
    let name = "Swan Yi Phyo"
    let age = 22
    // console.log(name)
    let handleClick = () => console.log("clicked")
    return{ name, age, handleClick }
  }
}
</script>
