<script>
  import TagsInput from './components/TagsInput.vue';

  export default {
    data: () => ({
      jsFrameworks: ["vue", "react.js", "angular"]
    }),
    mounted() {
      setTimeout(() => {
        this.jsFrameworks.push("svelte");
      }, 2000);
    }
  };
</script>

<template>
  <h1>Hello World</h1>
  <tags-input :selected-tags="jsFrameworks" @change=""/>
</template>

<style scoped>

</style>
