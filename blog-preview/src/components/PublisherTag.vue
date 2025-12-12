<template>
    <div class="publisher">
        <img src="../assets/images/profile.png" alt="Publisher profile picture"/>
        <div class="publisher-name"><slot /></div>
    </div>
</template>

<script>
export default {
    name: 'PublisherTag',
}
</script>

<style lang="scss" scoped>
@use '../assets/colors.scss' as *;
.publisher {
    display: flex;
    padding: 20px 0 2px 0;
}
img {
    width: 40px;
    height: 40px;
    object-fit: cover;
    border-radius: 50%;
    margin-right: 10px;
    display: block;
    flex-shrink: 0;
    align-self: center;
}
.publisher-name {
    color: $dark-grey;
    font-weight: bold;
    align-self: center;
}
</style>