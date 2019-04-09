<template>
  <nuxt-link :to="'/mission/' + id ">
    <article class="mission">
      <div class="thumbnail" :style="{backgroundImage: 'url(' + thumbnail + ')'}"></div>
      <h1>{{ title }}</h1>
      <p>{{ previewText }}</p>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  props: ["id", "thumbnail", "title", "previewText"]
};
</script>


<style scoped>
a {
  text-decoration: none;
  color: black;
}
.mission {
  box-sizing: border-box;
  width: auto;
  padding: 10px;
  border: 1px solid slategray;
  box-shadow: 4px;
  margin: 10px;
}

.thumbnail {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 200px;
}
</style>

