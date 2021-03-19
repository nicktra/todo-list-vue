<template>
    <div>
        <input class="form-check-input" onclick="" type="checkbox" value="" id="flexCheckDefault">
        <label class="form-check-label item" v-bind:class="{'item-completed':workItem.isDone}" for="flexCheckDefault">
            {{ workItem.name }}
        </label>
    </div>
</template>

<script>
export default {
    name: "ItemWork",
    props: ["workItem"]
}
</script>

<style scoped>

</style>