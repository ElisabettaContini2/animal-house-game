<template>
  <div>
    <b-sidebar
        id="sidebar-backdrop"
        backdrop
        shadow>
        <img src="../assets/logo.png" alt="logo" />
        <b-list-group>
          <b-list-group-item :to="{name: 'home'}">Home</b-list-group-item>
          <b-list-group-item :to="{name: 'about'}">Chi siamo</b-list-group-item>
          <b-list-group-item :to="{name: 'about'}">Scopri Animal House</b-list-group-item>
          <b-list-group-item :to="{name: 'my-animals'}">I miei animali</b-list-group-item>
          <b-list-group-item :to="{name: 'about'}">Gioca</b-list-group-item>
          <b-list-group-item :to="{name: 'about'}">Video</b-list-group-item>
          <b-list-group-item :to="{name: 'about'}">Informazioni sanitarie</b-list-group-item>
          <b-list-group-item :to="{name: 'about'}">Informazioni legali</b-list-group-item>
        </b-list-group>
    </b-sidebar>
  </div>
</template>

<script>
export default {
  name: 'MenuComponent',
  components: {
  },
  methods: {
  }
}
</script>

<style scoped>
a:active, a, a:focus {
  color: #495057;
  text-decoration: none;
}
</style>
