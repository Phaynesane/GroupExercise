<template>
    <div>
        <v-navigation-drawer width="250">
  <v-list-item title="My Application" subtitle="Vuetify"></v-list-item>
  <v-divider></v-divider>
  <v-list-item prepend-icon="mdi-home-city" title="Home" value="home" to="/">Home</v-list-item>
        <v-list-item prepend-icon="mdi-account" title="Manage" value="manage" to="/manage">Manage</v-list-item>
</v-navigation-drawer>
    </div>
</template>
<script>
export default {
    name: 'Sidebar',
}
</script>