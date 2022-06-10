<template>
  <div class="container">
      <div>{{details.title}}</div>
  </div>
</template>

<script>
export default {
  name: 'MyMusic',
  props: {
    details: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container{
    background-color: black;
}
</style>