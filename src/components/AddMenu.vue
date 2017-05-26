<template>
  <div class="hello">
  <h1>Subject</h1>
      <input v-model="name" type="text" class="form-control" placeholder="Subject Name" >
    <br>

<h1>Credit</h1>
     </div>  <select v-model="phone" class="form-control" placeholder="Credit" >
         <option value="1">1</option>
         <option value="3">3</option>
 </select><br>
 <h1>Grade</h1>
      <select v-model="email" type="text" class="form-control" placeholder="Grade"  >
        <option value="A">A</option>
        <option value="B+">B+</option>
        <option value="B">B</option>
        <option value="C+">C+</option>
        <option value="C">C</option>
        <option value="D+">D+</option>
        <option value="D">D</option>
         <option value="F">F</option>
      </select><!-- /input-group -->
   </div>
   <br>
   <span class="input-group-btn">
     <center><button @click="add(name, phone, email)" class="btn btn-default" type="button">Add Subject</button></center>
   </span>
  </div>
</template>

<script>
export default {
  props: ['add'],
  data () {
    return {
      input: ''
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
    background-color: #8B4513; /* Green */
    border: none;
    color: white;

    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
}
</style>
