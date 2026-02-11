<template>
    <div v-for="(tag, index) in tags"> {{ index + " : " + tag }} </div>
    <hr/>
    {{ newTag }}
    <input
        type="text"
        v-model.trim="newTag"
        @keydown.enter="tags.push($event.target.value)"
        @keydown.tab.prevent="tags.push($event.target.value)"
    />
</template>

<script>
export default {
    data: () => ({
        tags: ["vue", "react", "angular"],
        newTag: "test"
    }),
}
</script>