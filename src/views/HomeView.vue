<template>
  <div class="home">
    <h1>Home</h1>
    <div v-if="isShow">
      <PostsList :posts="posts"></PostsList>
    </div>
    <button @click="isShow = !isShow">{{ isShow ? 'Hide' : 'Show' }}</button>
    <button @click="posts.pop()">Delete</button>
  </div>
</template>

<script>
import PostsList from '../components/PostsList'
import { onMounted, onUnmounted, ref } from 'vue';


export default {
  components: { PostsList },
  setup() {
    let isShow = ref(true)
    let posts = ref([
      {
        id: 1,
        title: 'Post 1',
        content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis atque voluptatem nisi praesentium non esse? Adipisci ullam maiores consequatur, voluptatum repudiandae doloribus similique quaerat doloremque pariatur facere possimus magnam assumenda!'
      },
      {
        id: 2,
        title: 'Post 2',
        content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis atque voluptatem nisi praesentium non esse? Adipisci ullam maiores consequatur, voluptatum repudiandae doloribus similique quaerat doloremque pariatur facere possimus magnam assumenda!'
      },
      {
        id: 3,
        title: 'Post 3',
        content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis atque voluptatem nisi praesentium non esse? Adipisci ullam maiores consequatur, voluptatum repudiandae doloribus similique quaerat doloremque pariatur facere possimus magnam assumenda!'
      }
    ])
    
    
    

    return { posts, isShow }
  }
}
</script>

<style></style>
