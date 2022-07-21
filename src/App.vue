<template>
    <Navbar />
    <Forms @add-data='addName'/>
    <Card v-for="friend of friends" :key="friend" :data='friend'/>
</template>

<script>
import Navbar from './components/friend_menu.vue'
import Forms from './components/friend_form.vue'
import Card from './components/friend_card.vue'
export default {
  components: {
    Navbar,
    Forms,
    Card,
  },

    data() {
      return {
        friends: [
          // {name: 'Ronan', description: 'The best', skills:['HTML','CSS', 'PHP']},
          // {name: 'Rady', description: 'The best', skills:['HTML','CSS']},
          // {name: 'Him', description: 'The best', skills:['HTML','CSS', 'JAVA']},
      ]
    }
  },
  methods: {
    addName(firstname, lastname, comment, check) {
      this.friends.push({FirstName: firstname, LastName: lastname, Comment: comment, CheckValue: check})
    }
  }
}
</script>

<style scoped>
body {
    padding: 0;
    margin: 0;
}
</style>
