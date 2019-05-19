<template>
  <div>
  <v-toolbar color='indigo' dark>
    <v-toolbar-side-icon></v-toolbar-side-icon>
    <v-toolbar-title color='white'>Data Monitoring System</v-toolbar-title>
    <v-spacer></v-spacer>
    <div class="hidden-sm-and-down">
      <router-link to='/home'>
      <v-btn flat>Home</v-btn>
      </router-link>
      <router-link to='/register'>
      <v-btn flat>Register</v-btn>
      </router-link>
      <router-link to='/users'>
      <v-btn flat>Admins</v-btn>
      </router-link>
      <router-link to='/'>
      <v-btn flat>Logout</v-btn>
      </router-link>
      </div>
  </v-toolbar>
  </div>
</template>

