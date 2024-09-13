<template>
  <h1>{{ post.title }}</h1>
  <p>{{ isShow ? post.body : cutPostBody }} <span @click="isShow = !isShow">{{ isShow ? '' : 'Show more' }}</span></p>
  
</template>

<script>
import { computed, ref } from 'vue';

export default {
    props : ['post'],
    setup(props){
        let isShow = ref(false)
        let cutPostBody = computed(() => {
            return props.post.body.substring(0, 100) + "..."
        })

        return { cutPostBody, isShow }
    }
}
</script>

<style>

</style>