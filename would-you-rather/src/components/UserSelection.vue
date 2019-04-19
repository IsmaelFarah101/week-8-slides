
<!-- For some reasons this component only loads on screen when i click it the vue js devtools i think it mught have something to do with the computed property -->

<template>
<ul>
    <li v-for="answer in answers" v-bind:key = "answer.id">
        {{answer.answer}}
    </li>
</ul>
</template>
<script>
export default{
    data(){
        return{
            answers: ([])
        }
    },
    computed: {
        addtolist(){
            //I take the data and push it throuugh a set to remove any objects with the same ID
        this.answers = Array.from(new Set(this.userSelection)) 
        }
        
    },
   
    props: {
        userSelection: Array
    },
  
}
</script>
<style>
</style>