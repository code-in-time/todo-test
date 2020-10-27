<template>
  <table class="table">
    <thead>
      <tr>
        <th>userId</th>
        <th>title</th>
        <th>completed</th>
        <th>button</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="item in allTodos" :key="item.id+item.title">
        <td>{{ item.userId }}</td>
        <td>{{ item.title }}</td>
        <td>{{ item.completed }}</td>
        <td><button v-on:click="say(item.userId)" type="button" class="btn btn-primary">select</button></td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  name: 'ToDo',
    props: ["allTodos"],
    methods: {
    say: function (userId) {
      console.log(userId)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
