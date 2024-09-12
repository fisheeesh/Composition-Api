<template>
  <div class="home">
    <!-- <h1>{{ name }}</h1> -->
    <input type="text" v-model="search">
    <p>Search Item - {{ search }}</p>
    <div v-for="name in filteredNames" :key="name">
      {{ name }}
    </div>
  </div>
</template>

<script>
import { computed, ref } from 'vue';

export default {
  setup() {
    // let name = computed(() => {
    //   return "Swan Yi Phyo"
    // })
    let search = ref('')
    let names = ref([
      'Swan Yi Phyo',
      'Hla Hla',
      'Tun Tun',
      'Su Su',
      'Maung Maung',
      'Kyaw Kyaw'
    ])

    //computed property has to return
    let filteredNames = computed(()=>{
      return names.value.filter(name => name.includes(search.value))
    })


    return { names, search, filteredNames }
  }
}
</script>
