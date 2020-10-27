<template>
  <ul class="list-group">
    {{username}}
    <li class="list-group-item">Cras justo odio <button type="button" class="btn btn-primary">select</button></li>
    <li class="list-group-item">Cras justo odio <button type="button" class="btn btn-primary">select</button></li>
    <li class="list-group-item">Cras justo odio <button type="button" class="btn btn-primary">select</button></li>
    <li class="list-group-item">Cras justo odio <button type="button" class="btn btn-primary">select</button></li>
    <li class="list-group-item">Cras justo odio <button type="button" class="btn btn-primary">select</button></li>
  </ul>
</template>

<script>
export default {
  name: 'ToDo',
    props: ["allTodos"],
  // props: {
  //   msg: String,
  //   username: String,
  //     props: ["allTodos"],
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .container {
    width: 200px;
    display: "inline-block";
  }
</style>
