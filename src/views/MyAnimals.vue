<template>
  <b-container>
    <b-row>
      <HeaderComponent></HeaderComponent>
    </b-row>
    <h2>I miei animali</h2>
    <div>
        <b-card
            v-for="animale in animali"
            :key="animale.id"
            :title="animale.nome"
            :sub-title="animale.specie"
            img-src="https://picsum.photos/600/300/?image=25"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem;"
            class="mb-2"
        >
            <b-card-text>
            Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
            </b-card-text>

            <b-button href="#" variant="primary">Modifica</b-button>
        </b-card>
    </div>
  </b-container>
</template>

<script>
// @ is an alias to /src
import HeaderComponent from '@/components/HeaderComponent.vue'

export default {
  name: 'MyAnimals',
  components: {
    HeaderComponent
  },
  data () {
    return {
      animali: [
        {
          id: 1,
          nome: 'Leila',
          specie: 'Cane',
          selected: 'F'
        },
        {
          id: 2,
          nome: 'Poppi',
          specie: 'Coniglio',
          selected: 'M'
        },
        {
          id: 3,
          nome: 'Polly',
          specie: 'Criceto',
          selected: 'F'
        },
        {
          id: 4,
          nome: 'Minù',
          specie: 'Gatto',
          selected: 'F'
        }
      ]
    }
  }
}
</script>

<style scoped>
.card {
    margin: 1rem auto;
}
</style>
