<template>
    <div v-for="(tag, index) in tags"> {{ index + " : " + tag }} </div>
    <input type="text" :value="newTag" v-on:keydown.enter="tags.push($event.target.value)" />
</template>

<script>
export default {
    data: () => ({
        tags: ["vue", "react", "angular"],
        newTag: "test"
    }),
}
</script>