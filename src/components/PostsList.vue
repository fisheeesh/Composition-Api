<template>
  <div v-for="post in posts" :key="post.id">
    <SinglePost :post="post"></SinglePost>
  </div>
</template>

<script>
import SinglePost from './SinglePost'
import { onMounted, onUnmounted, onUpdated } from 'vue';
export default {
  components: { SinglePost },
  props : ['posts'],
  setup(){
    onMounted(() => console.log("mounted"))
    onUnmounted(() => console.log("unmounted"))
    onUpdated(() => console.log("updated"))
  }
}
</script>

<style></style>