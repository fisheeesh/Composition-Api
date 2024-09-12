<template>
  <div class="home">
    <!-- <h1>Person One</h1>
    <p>{{ personOne.name }} - {{ personOne.age }}</p>
    <button @click="changeOne">Change One</button>

    <h1>Person Two</h1>
    <p>{{ personTwo.name }} - {{ personTwo.age }}</p>
    <button @click="changeTwo">Change Two</button> -->

    <h1>User One - {{ userOne }}</h1>
    <button @click="changeOne">Change One</button>
    <h1>User Two - {{ userTwo }}</h1>
    <button @click="changeTwo">Change Two</button>
  </div>
</template>

<script>
import { reactive, ref } from 'vue';
export default {
  setup() {
    // let personOne = ref({
    //   name: 'John',
    //   age: 25
    // })

    // let personTwo = reactive({
    //   name: "Jane",
    //   age: 26
    // }) 
    // // console.log(personTwo)
    // // console.log(personOne)

    // let changeOne = () => personOne.value.name = "Swan Yi Phyo"
    // let changeTwo = () => personTwo.name = "Fisheeesh"

    let userOne = ref("Swan Yi Phyo")
    let userTwo = reactive("Fisheeesh")

    let changeOne = () => userOne.value = "John"
    //this will not work cuz reactive can not be worked with primitive values
    let changeTwo = () => userTwo = "Jane"


    return { userOne, userTwo, changeOne, changeTwo }
  }
}
</script>
