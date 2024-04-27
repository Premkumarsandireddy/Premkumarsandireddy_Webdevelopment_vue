<template>
  <MyHeader Name="Cricket Worldcup Stats" myName="Sandireddy Prem Kumar" />
  <StatsBox :Stats = Stats />
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import StatsBox from './components/StatsBox.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    StatsBox
  },
  data(){
    return{
      Stats:[]
    }
  },
  methods:{
    //promises
    async fetchStats(){
      const res = await fetch('https://world-cup-stats-node-server.onrender.com/api');
      const data = await res.json();
      return data
    }
  },

  async created(){
    this.Stats = await this.fetchStats();
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color:#DFD0B8
}
*{
  margin: 0;
  padding: 0;
  
}
</style>
