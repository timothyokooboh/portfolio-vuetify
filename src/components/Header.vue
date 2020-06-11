<template>
  <div>
    <v-app-bar app class="white">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>
        <v-btn text class="title">
          <span>TIM</span>
          <span class="grey--text">CODE</span>
          <v-icon medium> mdi-adobe-acrobat</v-icon>
        </v-btn>
      </v-toolbar-title>
    </v-app-bar>
    <v-navigation-drawer app v-model="drawer" class="indigo">
       <v-layout column align-center>

        <v-flex class="mt-5">
          <v-avatar size="100">
            <img src="../images/bizcard.jpeg" alt="">
          </v-avatar>
          <p>
            <v-btn text class="title">
              <span class="white--text">TIM</span>
              <span class="grey--text">CODE</span>
              <v-icon medium> mdi-adobe-acrobat</v-icon>
             </v-btn>
          </p>
        </v-flex>

      </v-layout>
      <v-list v-for="(route, index) in routes" :key="index">
        <v-list-item-group>
          <v-list-item router :to="route.link">
            <v-list-item-icon>
              <v-icon class="white--text">{{route.icon}}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title class="white--text"> {{route.name}}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>

      <v-list>
        <v-list-item>
          <v-list-item-icon>
            <v-icon class="white--text">mdi-github</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <a href="https://github.com/timothyokooboh" class="white--text" style="text-decoration: none">GITHUB</a>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>
<script>
export default {
  data () {
    return {
      drawer: false,
      routes: [
        {link:'/', name:'HOME', icon: 'mdi-home-edit-outline'},
        {link:'/projects', name:'PROJECTS', icon: 'mdi-folder'},
        {link:'/contact', name:'CONTACT', icon: 'mdi-phone'},
      ]
    }
  }
}
</script>
<style>
  .img {
    object-fit: cover;
  }
</style>