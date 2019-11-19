<template>
  <div>
    <ul>
      <li v-for= "(animal, index) in animals" :key= "index">
        {{ animal.species + ': ' + animal.name + ', born: '}}{{ animal.dateOfBirth ? animal.dateOfBirth : "Unknown"}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return {
      animals: [
        {species: "tiger", name: "El tigre", dateOfBirth: new Date()} ,
        {species: "elephant", name: "Kiril", dateOfBirth: new Date()},
        {species: "lion", name: "Leo", dateOfBirth: new Date()},
        {species: "monkey", name: "D Luffy", dateOfBirth: new Date()},
        {species: "parrot", name: "Kiki"}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
  ul{
    list-style: none;
  }
  li {
  border: 1px solid black;
}
</style>
