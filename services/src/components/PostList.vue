<template>
    <h1>LISTADO DE POST</h1>
    <ul class="post-list"  >
        <li v-for="post in posts" :key="post.id">{{post.title}}</li>
    </ul>
</template >

<script lang="ts" setup>
import PostService from '@/services/PostServices'
import { defineComponent, onMounted } from 'vue'
const service = new PostService()
const posts = service.getPosts()

onMounted(async () => {
  await service.fetchAll()
})
</script>

<!-- SIN SETUP
<script lang="ts">
import PostService from '@/services/PostServices'
import { defineComponent, onMounted } from 'vue'

export default defineComponent({
  name: 'PostList',
  setup () {
    const service = new PostService()
    const posts = service.getPosts()

    onMounted(async () => {
      await service.fetchAll()
    })
    return { posts }
  }
})
</script> -->

<style scoped lang="scss">
.post-list{
  width: 95vw;
  height: 75px;
  padding: 20px;
  list-style-type: none;
}
.post-list li {
  padding: 10px;
  width: 100%;
  border: 1px solid #ccc;
  color: $red;
}
</style>
