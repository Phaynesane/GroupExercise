<template>
  <v-app>
    <v-main>
      

      <v-navigation-drawer
        permanent
        location="right"
      >
        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-home-city" title="Home" value="home" to ="/" ></v-list-item>
          <v-list-item prepend-icon="mdi-account" title="Manage" value="manage" to="/manage"></v-list-item>
        </v-list>
      </v-navigation-drawer>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
}
</script>
