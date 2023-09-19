<template>
<div class="main-container2">

    <div class="project-card" v-for="(items, index) in projectData.ProjectsArray" v-bind:key="items">
        <h2>{{ projectData.ProjectsArray[index].Title }}</h2>
        <img :src="projectData.ProjectsArray[index].Image" alt=""> 
        <p>{{ projectData.ProjectsArray[index].About }}</p>
        <div class="links">
            <a :href="projectData.ProjectsArray[index].Link1" target="_blank"><img src="../assets/github.webp"></a>
            <a :href="projectData.ProjectsArray[index].Link2" target="_blank"><img src="../assets/linkt.png"></a>
        </div>
    </div>

    
</div>

</template>

<script>
import jsonData from "./projects.json"
export default {
    data(){
        return{
            projectData: jsonData
        }
    }
}


</script>

<style>
    .project-card img {
        margin-top: 2%;
        height: 10rem;
        border-radius: 10%;
        box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
    }

    .project1 {
        height: rem;
    }


    .main-container2 {
        margin-top: 5%;
        margin-bottom: 18%;
        display: flex;
        justify-content: center;
        align-items: center;        
        flex-wrap: wrap;
      
    }

    .project-card {
        width: 200%;
        margin: 10%;
        padding: 10px;
        flex-wrap: 0 0 40%;
        background-color: 	#c0b8b8;
        border-radius: 25%;
        box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
        align-self: center;
        text-align: center;
    }

    .links img {
        
        height: 2rem;
        margin: 3px;
        border-radius: 25%;
        margin-right: 30px;
        
    }

    .links {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-end;
    }

    h2 {
        text-align: center;
    }

    p {
        text-align: center;
        margin-top: 2%;
    }

</style>