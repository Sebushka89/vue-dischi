<template>
  <div id="app">
    <Loader v-if="discs.length == 0" />
    <Header @search="searchSomething"/>
    <Main :discs="filteredDiscs"  />
  </div>
</template>

<script>
import axios from 'axios';
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Loader from './components/Loader.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Loader
  },
  data(){
    return{
      discs:[],
      inputSearch:''
    }
  },
  created() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) =>{
      this.discs = result.data.response
      this.searchSomething('')
    })
  },
  computed:{
    filteredDiscs(){
      return this.discs.filter((element)=> {
        return element.title.includes(this.inputSearch)
      })
    }
  },
  methods: {
    searchSomething(searchString) {
      this.inputSearch = searchString
    }
  }
}
</script>

<style lang="scss">

@import "./style/app.scss"


</style>
