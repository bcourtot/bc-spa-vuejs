<template>
    <div>
        <p class="article-content" :content="post.body">{{ content }}</p>
    </div>
</template>

<script>
    export default {
        props: {
            content: {
                type: String,
            },
        },
    }
</script>

<style lang="scss" scoped>
    .article-content {
        font-size: 15px;
        color: #181818;
        text-align: justify;
    }
</style>