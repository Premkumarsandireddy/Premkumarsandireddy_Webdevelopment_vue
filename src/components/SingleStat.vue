<template>
<div class="worldcupstats">
            <div class="box" id="box1">
                <h2>YEAR: {{Stat.year}}</h2>
                <p>Winning Team: {{Stat.country}}</p>
            </div>
            <div class="box">
                <p>Most Runs: {{Stat.MostRuns}}</p>
                <p>Most Wickets: {{Stat.MostWickets}}</p>   
                <p>PlayerofTheTournament: {{Stat.PlayerOfTheTournament}}</p>
            </div>
            <div class="box">
                <p>HostNation: {{Stat.HostNation}}</p>
                <p>MostHundreds: {{Stat.MostHundreds}}</p>
                <p>HighestScorer: {{Stat.HighestScorer}}</p>
            </div>
</div>
</template>
<script> 
    export default{
        name:'SingleStat',
        props:{
            Stat:Object
        }
    }
</script>
<style>
    p{
        font-family:Verdana, Geneva, Tahoma, sans-serif;
        font-size:20px;
        color:white;
        padding: 10px;
    }
    #year{
        color:rgb(129, 146, 45);
        text-decoration: underline;
        font-family:sans-serif;
    }
    .worldcupstats{
        display: flex;
        background-color:#153448;
        border-radius: 30px;
        margin: 10px;
    }   
    .box{
        height:100%;
        width:100%;
        margin-top: 20px;
        padding: 10px;

    }
    h2{
        color:#DFD0B8;
        font-size: 30px;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        margin:15px;
    }

</style>