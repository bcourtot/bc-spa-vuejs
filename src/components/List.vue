<template>
  <div class="container">
    <div>
    <h1>Liste des articles</h1>
      <ul class="list">
        <div v-if="posts.length > 0">
            <li v-for="post in posts" :key="post.title" class="list-item">
                <ArticleTitle :postId="post.id" :title="post.title"></ArticleTitle>
            </li>
        </div> 
      </ul>
    </div>
</div>
</template>

<script>
    import axios from "axios";
    import ArticleTitle from '../components/ArticleTitle.vue'

    export default {
    components: { ArticleTitle },
    data() {
        return {
        posts: [],
        };
    },
    mounted() {
        axios
        .get("https://jsonplaceholder.typicode.com/posts")
        .then((response) => (this.posts = response.data));
    },
    };
</script>

<style lang="scss" scoped>
    .container {
        max-width: 85%;
        margin: 0 auto;
    }

    .list {
        list-style: none;
        text-align: start;
    }

    .list-item {
        margin: 80px;
    }

    h1 {
        font-size: xx-large;
    }


</style>