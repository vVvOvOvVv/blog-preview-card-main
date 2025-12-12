<template>
    <div class="img-template">
        <img src="../assets/images/illustration-article.svg" :alt="imgAlt" />
    </div>
</template>

<script>
export default {
    name: 'ImageTemplate',
    props: {
        imgAlt: {
            type: String,
            required: false,
            default: 'Blog preview cover image',
        },
    },
}
</script>

<style lang="scss" scoped>
img {
    width: 100%;
    margin: 1px;
    height: auto;
    border-radius: 15px;
    background-position: center;
}
</style>