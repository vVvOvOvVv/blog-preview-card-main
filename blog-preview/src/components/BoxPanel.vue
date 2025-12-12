<template>
    <div class ="box-panel">
        <slot name="picture"/>
        <div class="tags"><slot name="tag"/></div>
        <div class="publish-date">
            <slot name="publish-date" />
        </div>
        <div class="title">
            <slot name="title"/>
        </div>
        <div class="desc">
            <slot name="desc"/>
        </div>
        <div class="publisher">
            <slot name="publisher"/>
        </div>
    </div>
</template>

<script>
export default {
    name: 'BoxPanel',
}
</script>

<style lang="scss" scoped>
@use '../assets/colors.scss' as *;
.box-panel {
    background-color: white;
    border-radius: 15px;
    box-shadow: 10px 15px 0 $dark-grey;
        // horizontal vertical blur color
    outline: $dark-grey 2px solid;
    padding: 20px;
    width: 50vw;
    min-width: 270px;
    max-width: 400px;
    margin: 40px auto;
    transition: transform 0.3s ease-in-out; /* Smooth transition for the transform property */
    &:hover {
    transform: scale(1.01); /* Enlarge to 120% of its original size */
    }
}

.tags {
    display: flex;
    gap: 10px;
    padding: 15px 0;
    flex-wrap: wrap;
}

.publish-date { // ig setup like this needs to apply to the parent div
    color: $dark-grey;
    text-align: left;
}

.title {
    font-size: 1.5rem;
    font-weight: bold;
    color: $dark-grey;
    padding: 15px 0;
    text-align: left;
    &:hover {
        color: $primary-color;
    }
}

.desc {
    color: $light-grey;
    text-align: left;
}
</style>