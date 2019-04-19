<template>
<div id="app">
<div>
    <h2>{{question.question}}</h2>
    <input type='radio' v-model="choice.answer" v-bind:value="question.answer1" v-on:change="$emit('answer-changed', choice)">
    <label>{{question.answer1}}</label>
    <input type="radio" v-model="choice.answer" v-bind:value="question.answer2" v-on:change="$emit('answer-changed', choice)">
    <label>{{question.answer2}}</label>
</div>
</div>

</template>
<script>
export default{
    data(){
        return{
            choice: {
                id: this.question.id,
                answer: ''
            }
        }
    },
    props: {
        question: Object

    },
  
}

</script>
<style>

</style>