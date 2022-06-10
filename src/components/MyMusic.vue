<template>
  <div class="card">
      
    <img :src="details.poster" alt="">
    <div>{{details.title}}</div>
    <div>{{details.author}}</div>
    <div>{{details.year}}</div>



  </div>
</template>

<script>
export default {
  name: 'MyMusic',
  props: {
    details: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.card{
    background-color: rgba(45, 90, 141, 0.452);
    width: 150px;
    min-height: 150px;
    display: inline-block;
    margin: 15px;
    color: black;
}
img {
    width: 75%;
    height: 75%;
}
</style>