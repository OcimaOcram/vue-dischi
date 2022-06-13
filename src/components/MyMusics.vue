<template>
   <main>

        <SearchMusic @selected="changeSelect"/>
        <section>
            <MyMusic
                v-for="(music, i) in filteredmusicList"
                :key="i"
                :details="music"
            />
        </section>
    </main>
</template>

<script>
import axios from "axios"
import MyMusic from "./MyMusic.vue";
import SearchMusic from "./SearchMusic.vue";

export default {
  name: 'MyMusics',
  components: {
    MyMusic,
    SearchMusic
},
 data() {
        return {
            apiUrl: 'https://flynn.boolean.careers/exercises/api/array/music',
            musicList: [],
            selected : ''
        }
    },
    created() {
        this.getMusic();
    },
    computed : {
        
        filteredmusicList(){
            if (this.selected === 'all') {
                return this.musicList
            }
            return this.musicList.filter((item) => {
                return item.genre.includes(this.selected)
            })
        }
    },
    methods: {
        
        getMusic() {
            axios
            .get(this.apiUrl)
            .then((result) => {
                this.musicList = result.data.response
            })
        },
        
        changeSelect(selezione){
            this.selected = selezione
            console.log(this.selected);
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
main{
    background-color: rgb(28, 40, 61);
}
</style>
