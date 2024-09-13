<template>
  <h1>{{ post.title }}</h1>
  <p>{{ isShow ? post.body : cutPostBody }} <span @click="isShow = !isShow">{{ isShow ? '' : 'Show more' }}</span></p>
  
</template>

<script>
import { computed, onMounted, onUnmounted, onUpdated, ref } from 'vue';

export default {
    props : ['post'],
    setup(props){
        let isShow = ref(false)
        let cutPostBody = computed(() => {
            return props.post.body.substring(0, 100) + "..."
        })

        onMounted(() => console.log("mounted"))
        onUnmounted(() => console.log("unmounted"))
        onUpdated(() => console.log("updated"))

        return { cutPostBody, isShow }
    }
}
</script>

<style>

</style>