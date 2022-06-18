<template>
    <b-container>
        <b-button @click="getGames"></b-button>
        <b-button @click="getMemes"></b-button>
    </b-container>
</template>

<script>
export default {
  name: 'GameView',
  components: {
  },
  data () {
  },
  methods: {
    getGames () {
      fetch('https://zoo-animal-api.herokuapp.com/animals/rand/5')
        /* .then(response => response.json()) */
        .then(response => console.log(response))
        .catch(err => console.error(err))
    },
    getMemes () {
      fetch('https://api.imgflip.com/get_memes')
        /* .then(response => response.json()) */
        .then(response => console.log(response))
        .catch(err => console.error(err))
    }
  }
}
</script>
