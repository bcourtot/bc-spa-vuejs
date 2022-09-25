<template>
  <div class="article-item">
    <span class="article-lettrine">{{ title.charAt(0) }}</span>
    <span class="article-title"><router-link class="link" to="article/{postId}">{{ title }}</router-link></span>
  </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
        },
        postId: {
            type: Number,
        }
    },
};
</script>

<style lang="scss" scoped>
.article-lettrine {
  font-size: x-large;
  margin-right: 60px;
  background-color: crimson;
  color: snow;
  padding: 20px;
  border-radius: 50%;
  text-transform: uppercase;
}

.article-title {
  font-family: Arial, Helvetica, sans-serif;
  font-size: x-large;
}

.link {
  text-decoration: none;
  color: rgb(95, 95, 95);
}
</style>