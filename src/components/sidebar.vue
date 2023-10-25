<template>
    <v-main style="height: 650px; display: flex; justify-content: center;">
      <v-app-bar
        color="primary"
        prominent
      >
        <v-app-bar-nav-icon variant="text" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
  
        <v-toolbar-title>Trinity</v-toolbar-title>
      </v-app-bar>
  
      <v-navigation-drawer
        v-model="drawer"
        location="left"
        temporary
      >
        <v-list>
          <v-list-item prepend-icon="mdi-home-city" title="Home" @click="showHomeContent = true"></v-list-item>
          <v-list-item prepend-icon="mdi-account" title="Manage" @click="showHomeContent = false"></v-list-item>
        </v-list>
      </v-navigation-drawer>
  
      <v-card-text>
        <div style="text-align: center; padding: 10px 20px;">
          <div v-if="showHomeContent">
            <!-- Content for the "Home" page -->
            "The Trinity" is a dynamic and closely-knit group of three individuals, 
            each bringing their unique talents, skills, and personalities to create 
            a formidable team. <br> This triad operates in perfect harmony, mirroring 
            the concept of the Holy Trinity. Each member of "The Trinity" complements 
            the others, resulting in a synergy <br>that leads to exceptional teamwork, 
            problem-solving, and shared successes.
          </div>
          <div v-else>
            -            <!-- Content for the "Manage" page -->     
            <div class="max-w-2xl">
                <h1 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Meet our Group</h1>
                <p class="mt-6 text-lg leading-8 text-gray-600">“We’re excited to have you visit us and hope you’ll have a wonderful time.
                     We believe that each of us has unique abilities, and effective communication is essential to harnessing our distinct 
                     features for the success of our upcoming projects.”</p>
            </div>
            <v-container>
                <v-row>
                <v-col
                    cols="12"
                    sm="6"
                    md="4"
                    v-for="person in [
                    {
                        name: 'Jhon Melvin B Jambalos',
                        role: 'Programmer',
                        imageUrl: require('@/assets/Images/melvz.png.jpg'),
                        name: 'Hanie Jean Bueno',
                        role: 'Programmer',
                        imageUrl: require('@/assets/Images/hanie.png.jpg'),
                    },
                    {
                        name: 'Maricon Barcibal',
                        role: 'Programmer',
                        imageUrl: require('@/assets/Images/con.png.jpg'),
                    },
                    // Add more people and their image URLs as needed
                    ]"
                    :key="person.name"
                >
                  <v-card>
                  <v-img :src="person.imageUrl" alt="Person's Image" class="rounded-lg"></v-img>
                  <v-card-title class="text-h6">{{ person.name }}</v-card-title>
                  -                  <v-card-text>{{ person.role }}</v-card-text>
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