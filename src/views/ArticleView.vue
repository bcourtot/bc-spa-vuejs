<template>
  <div>
    <ArticleTitle :title="post.title"></ArticleTitle>
    <ArticleBody :content="post.content"></ArticleBody>
    <ArticleComment></ArticleComment>
    {{ post }}
  </div>
</template>

<script>
import ArticleTitle from "@/components/ArticleTitle.vue";
import ArticleBody from "@/components/ArticleBody.vue";
import ArticleComment from "@/components/ArticleComment.vue";
export default {
  components: { ArticleTitle, ArticleBody, ArticleComment },
}

</script>

<style lang="scss" scoped>
</style>