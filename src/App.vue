<template>
  <div id="app">
    <h2>
      What I Do Today?
    </h2>

    <div v-for="workItem in work" v-bind:key="workItem.id" class="work">
      <p>{{ workItem.name }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: function() {
    return {
      work: [
        {
          id: 1,
          name: "Cleaning Room"
        }
      ]
    };
  },
  components: {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
