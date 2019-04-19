<template>
  <div id="app">
    <WouldYouRather v-for="question in questions" v-bind:key = "question.id" v-bind:question = "question"  v-on:answer-changed="answerChanged">
    </WouldYouRather>
    <UserSelection v-bind:userSelection = "userselection">
    </UserSelection>
  </div>

</template>

<script>
import WouldYouRather from './components/WouldYouRather.vue'
import UserSelection from './components/UserSelection.vue'
export default {
  name: 'app',
  components: {
    WouldYouRather,
    UserSelection
  },
  data(){
    return {
      userselection: [],
      questions: [
        {
          id: 0,
          question: "Live in a Triangle Shaped House or a circle shaped house",
          answer1: "Triangle Shaped",
          answer2: "Circle Shaped"
        },
        {
         id: 1,
          question: "Be a wizard or a superhero",
          answer1: "Wizard",
          answer2: "Superhero"

        },
        {
          id: 2,
          question: "Have a Elephant sized-cat or a Cat sized-elephant",
          answer1: "Elephant sized-cat",
          answer2: "Cat sized-elephant"
        }
      ]
    }

  },
      methods : {
        answerChanged(answer){
          this.userselection.push(answer)

          
      }
  }
    }

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
