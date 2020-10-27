<template>
  <div id="app" class="container">
    <div class="row">
      <div class="col">
        <ToDo username='matt' v-bind:allTodos="allTodos" showCompleted="false"/>
      </div>
      <div class="col">
        <ToDo username='matt' v-bind:allTodos="allTodos" showCompleted="true"/>
      </div>
    </div>
  </div>
</template>

<script>
import ToDo from './components/ToDo.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    ToDo
  },
  data () {
    return {
      allTodos: [
        {completed: false, id: 1, title: "delectus aut autem", userId: 1 }
      ]
    }
  },
  mounted () {
    console.log('mounted')
    this.fetchAPIData()
  },
  methods: {
    fetchAPIData() {
      axios
        .get('https://jsonplaceholder.typicode.com/todos')
        .then(response => {
          console.log('this.allTodos', this.allTodos)
          this.allTodos = response.data
      })
    }
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
}


</style>
