<template>
    <div class="tag-box">
        <b><slot /></b>
    </div>
</template>

<script>
export default {
    name: 'TagBox',
}
</script>

<style lang="scss" scoped> 
@use '../assets/colors.scss' as *;
.tag-box {
    background-color: $primary-color;
    padding: 5px 10px; // top-bottom 5px, left-right 10px
    margin: 0;
    max-width: fit-content;
    align-items: center;
    border-radius: 5px;
    color: $dark-grey;
}
</style>