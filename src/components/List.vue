<template>
  <div class="hello">
    <table class="table" align="center">
      <tbody>
        <tr>
          <th scope="row" width="200px">{{index+1}}</th>
          <td width="200px">{{list.name}}</td>
          <td width="200px">{{list.phone}}</td>
          <td width="200px">{{list.email}}</td>
          <td>  <button @click="remove(index)" class="btn btn-danger" >Delete Subject</button></td>
        </tr>

      </tbody>
    </table>


  <!-- {{list.name}}
  {{list.phone}}
  {{list.email}}
    <button @click="remove(index)">X</button>
  </div> -->
</template>

<script>
export default {
  props: ['list', 'remove', 'index'],
  data () {
    return {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: #42b983;
}
button {
    background-color: #4CAF50; /* Green */
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
}
</style>
