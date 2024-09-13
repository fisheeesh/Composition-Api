<template>
    <h1>{{ post.title }}</h1>
    <p @click="isShow = !isShow">{{ isShow ? post.content : cutBodyPost }}</p>
</template>

<script>
import { computed, ref } from 'vue';

export default {
    props : [
        'post'
    ],
    setup(props){
        // console.log(props.post.title)
        let isShow = ref(false)
        let cutBodyPost = computed(()=> props.post.content.substring(0, 100) + "...")

        return { cutBodyPost, isShow}
    }
}
</script>

<style>

</style>