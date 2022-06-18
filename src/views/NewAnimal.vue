<template>
  <b-container>
    <b-row>
      <HeaderComponent></HeaderComponent>
    </b-row>
    <h2 class="text-center">Nuovo Animale</h2>
    <div>
      <b-form @submit="onSubmit" @reset="onReset" v-if="show" class="text-left">
        <b-form-group id="input-group-1" label="Nome" label-for="input-1">
          <b-form-input
            id="input-1"
            v-model="form.nome"
            placeholder="Inserisci nome"
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Specie" label-for="input-2">
          <b-form-select
            id="input-2"
            v-model="form.specie"
            :options="specie"
            required
          ></b-form-select>
        </b-form-group>

        <b-form-group id="input-group-3" label="Seleziona il sesso" v-slot="{ ariaDescribedby }">
          <b-form-radio v-model="form.selected" :aria-describedby="ariaDescribedby" name="some-radios" value="M">Maschio</b-form-radio>
          <b-form-radio v-model="form.selected" :aria-describedby="ariaDescribedby" name="some-radios" value="F">Femmina</b-form-radio>
        </b-form-group>

        <b-button type="submit" variant="primary" class="btn-submit">Submit</b-button>
        <b-button type="reset" variant="danger">Reset</b-button>
      </b-form>
    </div>
  </b-container>
</template>

<script>
// @ is an alias to /src
import HeaderComponent from '@/components/HeaderComponent.vue'

export default {
  name: 'NewAnimal',
  components: {
    HeaderComponent
  },
  data () {
    return {
      form: {
        nome: '',
        specie: null,
        selected: ''
      },
      specie: [{ text: 'Seleziona la specie', value: null }, 'Cane', 'Gatto', 'Coniglio', 'Criceto'],
      show: true
    }
  },
  methods: {
    onSubmit (event) {
      event.preventDefault()
      /* alert(JSON.stringify(this.form)) */
      console.log(JSON.stringify(this.form))
    },
    onReset (event) {
      event.preventDefault()
      // Reset our form values
      this.form.nome = ''
      this.form.specie = null
      this.form.selected = ''
      // Trick to reset/clear native browser form validation state
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
      console.log(JSON.stringify(this.form))
    }
  }
}
</script>

<style scoped>
.btn-submit {
  margin-right: 1rem;
}
</style>
