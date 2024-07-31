<template>
  <div class="post-card">
    <h3>Titulo</h3>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Tenetur,
      incidunt! Dolores deserunt ex placeat saepe, rerum et qui soluta. Unde
      quia ipsam quod quisquam, voluptas sed porro autem labore laboriosam.
    </p>
    <PostButton />
  </div>
</template>

<script lang="ts" setup>
import PostButton from "./PostButton.vue";
</script>

<style scoped>
.post-card {
  border-radius: 15px;
  padding: 10px;
  margin: 5px;
  border: 1px solid #ccc;
}
</style>
