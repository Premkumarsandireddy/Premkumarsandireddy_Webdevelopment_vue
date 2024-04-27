<template>
    <div v-for="Stat of Stats " :key="Stat.id">
      <SingleStat :Stat=Stat />
    </div>

</template>

<script>
 import SingleStat from './SingleStat.vue'

export default {
  name: 'StatsBox',
  props:{
    Stats:Array
  },
  components:{
    SingleStat
  }
}
</script>

<style>
      
</style>