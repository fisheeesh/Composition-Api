<template>
  <h1>Posts List</h1>
  <div v-for="post in posts" :key="post.id">
    <div v-if="isShow">
      <SinglePost :post="post"></SinglePost>
    </div>
  </div>
  <button @click="isShow = !isShow">Show</button>
</template>

<script>
import { ref } from 'vue';
import SinglePost from './SinglePost'
export default {
  components: { SinglePost },
  props: ['posts'],
  setup(props){
    let isShow = ref(false)
    // console.log(props.posts[0].title)

    return { isShow }
  }
}
</script>

<style>

</style>