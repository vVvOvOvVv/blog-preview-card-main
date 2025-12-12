<template>
  <box-panel>
    <template v-slot:picture>
      <ImageTemplate /> <!--idk why img-template isn't working-->
    </template>
    <template v-slot:tag>
      <tag-box>Learning</tag-box>
    </template>
    <template v-slot:publish-date>
      Published 10 Nov 2025
    </template>
    <template v-slot:title>
      HTML & CSS foundations
    </template>
    <template v-slot:desc>
      These languages are the backbone of every website, defining structure, content, and presentation.
    </template>
    <template v-slot:publisher>
      <publisher-tag>Frontend Mentor Challenge</publisher-tag>
    </template>
  </box-panel>
</template>

<script>
import BoxPanel from './components/BoxPanel.vue'
import ImageTemplate from './components/ImageTemplate.vue';
import TagBox from './components/TagBox.vue';
import PublisherTag from './components/PublisherTag.vue';

export default {
  name: 'App',
  components: {
    BoxPanel,
    ImageTemplate,
    TagBox,
    PublisherTag,
  }
}
</script>

<style lang="scss">
@use './assets/colors.scss' as *;

html {
  background-color: $primary-color;
  color: $dark-grey;
  font-size: 16px;
}
</style>
