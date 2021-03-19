<template>
  <div id="app">
    <div class="container">
      <div class="row header mb-5 p-3">
        <div class="col-lg-12">
          <h2>What I Do Today?</h2>
        </div>
      </div>
      <div class="row content">
        <div class="col-lg-12">
          <div class="work-home">
            <div class="row">
              <div v-for="workItem in work" v-bind:key="workItem.id" class="mb-4 work col-lg-12 text-left">
                <ItemWork v-bind:workItem="workItem" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css"
import ItemWork from './components/ItemWork.vue';

export default {
  name: 'App',
  data: function() {
    return {
      work: [
        {
          id: 1,
          name: "Cleaning Room",
          isDone: false
        },
        {
          id: 2,
          name: "Jogging 5 km",
          isDone: false
        },
        {
          id: 3,
          name: "Lunch with family",
          isDone: false
        },
        {
          id: 4,
          name: "Coding",
          isDone: false
        }
      ]
    };
  },
  components: {
    ItemWork
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

.header {
  background: #1abc9c;
}

.header h2 {
  margin: 0;
}

.work .item {
  font-size: 20px;
}

.item-completed {
  color: #1abc9c;
}
</style>
