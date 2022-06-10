<template>
  <div class="container">
      <MyMusic/>
  </div>
</template>

<script>
import axios from "axios"
import MyMusic from "./MyMusic.vue";

export default {
  name: 'MyMusics',
  components: {
    MyMusic
},
  data () {
      return {
          apiUlr: "https://flynn.boolean.careers/exercises/api/array/music",
          musicsList: []
      }
  },
  created () {
      axios.get(this.apiUlr)
      .then((result) =>{
          this.musicsList = result.data;
          console.log(result);
      })
      .catch((error) =>{
      
      console.log("Errore", error);
      
  })

  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container{
    background-color: black;
}
</style>
