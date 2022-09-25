<template>
    <div class="container">
        <h3>Commentaires</h3>
        <div v-if="comments.length > 0">
            <div v-for="comments in comment" :key="comment.title">
                <h5 :title="comment.title"></h5>
                <a href="mailto:" :mail="comment.mail">{{ mail }}</a>
                <p> {{ comment }}</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            propName: {
                type: Number,
            },
        },
    }
</script>

<style lang="scss" scoped>
    .container {
        max-width: 95%;
        margin: 0 auto;
        text-align: start;
    }

    h3 {
        text-decoration: underline;
    }

    h5 {
        font-weight: 900;
    }

    p {
        font-size: 10px;
    }

</style>