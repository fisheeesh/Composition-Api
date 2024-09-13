<template>
  <div class="home">
    <PostsList :posts="posts"></PostsList>
  </div>
</template>

<script>
import PostsList from '../components/PostsList'
import { ref } from 'vue';


export default {
  components: { PostsList },
  setup() {
    let posts = ref([
      { id: 1, title: "post 1", body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor, exercitationem repellendus dolores veritatis dicta cumque nam sunt ea sit, nesciunt, provident ratione amet a nulla iure adipisci dolore autem. Sint suscipit deserunt ratione iusto molestias dolores dignissimos alias. Temporibus soluta quam adipisci numquam voluptas ipsam, aut aspernatur ipsa unde impedit autem libero! Illo modi maxime ipsa libero? Non aut nihil nesciunt veniam sapiente, provident blanditiis possimus ducimus repudiandae et. Animi officia impedit repudiandae rem soluta nesciunt tempora ipsam, ex aspernatur praesentium voluptatem facere, porro in quae possimus sit vel ducimus unde perspiciatis. Quis perferendis velit aperiam non explicabo, voluptate impedit tenetur porro. Nobis eaque quos voluptas, labore animi atque praesentium. Facere, fugiat? Et repellat fuga quibusdam iste vitae laboriosam facere nihil nesciunt? Voluptas magni, exercitationem atque, quidem officia dignissimos at commodi suscipit aperiam beatae quam quaerat est hic mollitia, quisquam repellendus sequi expedita autem? Commodi distinctio perspiciatis animi provident eligendi!" },
      { id: 2, title: "post 2", body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor, exercitationem repellendus dolores veritatis dicta cumque nam sunt ea sit, nesciunt, provident ratione amet a nulla iure adipisci dolore autem. Sint suscipit deserunt ratione iusto molestias dolores dignissimos alias. Temporibus soluta quam adipisci numquam voluptas ipsam, aut aspernatur ipsa unde impedit autem libero! Illo modi maxime ipsa libero? Non aut nihil nesciunt veniam sapiente, provident blanditiis possimus ducimus repudiandae et. Animi officia impedit repudiandae rem soluta nesciunt tempora ipsam, ex aspernatur praesentium voluptatem facere, porro in quae possimus sit vel ducimus unde perspiciatis. Quis perferendis velit aperiam non explicabo, voluptate impedit tenetur porro. Nobis eaque quos voluptas, labore animi atque praesentium. Facere, fugiat? Et repellat fuga quibusdam iste vitae laboriosam facere nihil nesciunt? Voluptas magni, exercitationem atque, quidem officia dignissimos at commodi suscipit aperiam beatae quam quaerat est hic mollitia, quisquam repellendus sequi expedita autem? Commodi distinctio perspiciatis animi provident eligendi!" },
      { id: 3, title: "post 3", body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor, exercitationem repellendus dolores veritatis dicta cumque nam sunt ea sit, nesciunt, provident ratione amet a nulla iure adipisci dolore autem. Sint suscipit deserunt ratione iusto molestias dolores dignissimos alias. Temporibus soluta quam adipisci numquam voluptas ipsam, aut aspernatur ipsa unde impedit autem libero! Illo modi maxime ipsa libero? Non aut nihil nesciunt veniam sapiente, provident blanditiis possimus ducimus repudiandae et. Animi officia impedit repudiandae rem soluta nesciunt tempora ipsam, ex aspernatur praesentium voluptatem facere, porro in quae possimus sit vel ducimus unde perspiciatis. Quis perferendis velit aperiam non explicabo, voluptate impedit tenetur porro. Nobis eaque quos voluptas, labore animi atque praesentium. Facere, fugiat? Et repellat fuga quibusdam iste vitae laboriosam facere nihil nesciunt? Voluptas magni, exercitationem atque, quidem officia dignissimos at commodi suscipit aperiam beatae quam quaerat est hic mollitia, quisquam repellendus sequi expedita autem? Commodi distinctio perspiciatis animi provident eligendi!" },
    ])

    return { posts }
  }
}
</script>
