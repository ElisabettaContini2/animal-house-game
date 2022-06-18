<template>
    <b-container>
        <b-row>
            <b-button v-b-toggle.sidebar-backdrop>
                <b-icon-list></b-icon-list>
            </b-button>
            <img src="../assets/logo.png" alt="logo">
            <b-button>
                <b-icon-person></b-icon-person>
            </b-button>
        </b-row>
        <MenuComponent></MenuComponent>
    </b-container>
</template>

<script>
import MenuComponent from './MenuComponent.vue'

export default {
  name: 'HeaderComponent',
  components: {
    MenuComponent
  }
}
</script>

<style scoped>
.container {
    background-color: lightgray;
    margin: 0;
    width: 100%;
    max-width: 100%;
    padding: 0 1rem;
}
.row {
    margin: 0;
    padding: 1rem 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
img {
    width: 2rem;
    height: 2rem;
}
</style>
