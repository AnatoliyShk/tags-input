<script>
  import TagsInput from './components/TagsInput.vue';

  export default {
    data: () => ({
      jsFrameworks: ["vue", "react.js", "angular"],
      backendFrameworks: []
    }),
    methods: {
      handleChange(tags) {
        this.jsFrameworks = [...tags];
      }
    },
  };
</script>

<template>
  <h1>Your favorite frameworks</h1>
  <div>{{  jsFrameworks }}</div>
  <tags-input :selected-tags="jsFrameworks" @change="handleChange"/>

    <div>{{  backendFrameworks }}</div>
  <tags-input :selected-tags="backendFrameworks" @change="handleChange"/>
</template>

<style scoped>

</style>
