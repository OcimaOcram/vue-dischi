<template>
  <div class="select">
      
      <select name="genre" id="genre" v-model="userSelect" @change="$emit('selected', userSelect)">
        <option value="all">Tutti</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
      </select>
    </div>
</template>

<script>
   export default {
    name: 'SearchMusic',
        data() {
            return {
                
                userSelect : '',
            }
        }
    }

</script>


<style scoped lang="scss">
.container{
    background-color: rgb(28, 40, 61);
}
</style>