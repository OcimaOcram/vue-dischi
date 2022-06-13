<template>
  <div class="card">
      
        <img :src="details.poster" :alt="details.title">
        <h3>{{details.title.toUpperCase()}}</h3>
        <span>{{details.author}}</span>
        <span>{{details.year}}</span>
  </div>
</template>

<script>
export default {
  name: 'MyMusic',
  props: {
      details: Object,
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
    margin-top: 15px;
    width: 75%;
    height: 75%;
}
</style>