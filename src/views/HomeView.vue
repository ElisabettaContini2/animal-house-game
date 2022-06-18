<template>
  <b-container>
    <b-row>
      <HeaderComponent></HeaderComponent>
    </b-row>
    <b-row>
      <b-button @click='toNewAnimal()'>Aggiungi un animale</b-button>
      <!-- <b-button @click='callImg()'>animale</b-button> -->
    </b-row>
  </b-container>
</template>

<script>
// @ is an alias to /src
import HeaderComponent from '@/components/HeaderComponent.vue'

export default {
  name: 'HomeView',
  components: {
    HeaderComponent
  },
  data () {
    return {
    }
  },
  methods: {
    toNewAnimal () {
      this.$router.push({ path: '/new-animal' })
    }
    /* callImg () {
      this.responseAvailable = false
      fetch('https://jokes-database.p.rapidapi.com/', {
        method: 'GET',
        headers: {
          'x-rapidapi-host': 'jokes-database.p.rapidapi.com',
          'x-rapidapi-key': this.apiKey
        }
      })
        .then(response => {
          if (response.ok) {
            return response.json()
          } else {
            alert('Server returned ' + response.status + ' : ' + response.statusText)
          }
        })
        .then(response => {
          this.result = response.body
          this.responseAvailable = true
        })
        .catch(err => {
          console.log(err)
        })
    } */
  }
}
</script>

<style scoped>
</style>
