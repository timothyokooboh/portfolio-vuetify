<template>
  <div class="home">
    <div id="bio">
      <div class="image-container mt-2" id="bio-content">
        <v-avatar size="150">
          <img src="images/profile.jpg">
        </v-avatar>
        <div class="font-weight-bold py-3">TIMOTHY <span class="grey--text">OKOOBOH</span></div>
        <div class="font-weight-bold pb-3">FULL STACK <span class="grey--text">SOFTWARE ENGINEER</span></div>
        <div>
          <a href="https://github.com/timothyokooboh" target="_blank">
            <v-icon color="white" class="mx-2 github-linkedin">mdi-github</v-icon>
          </a>
          <a href="https://linkedin.com/in/timothy-okooboh-193980165/" target="_blank">
            <v-icon color="white" class="mx-2 github-linkedin">mdi-linkedin</v-icon>
          </a>
          <a href="https://twitter.com/inspiretim24" target="_blank">
           <v-icon color="white" class="mx-2 twitter-email">mdi-twitter</v-icon>
          </a>
          <a href="mailto:okoobohtimothy@gmail.com" target="_blank">
            <v-icon color="white" class="mx-2 twitter-email">mdi-email</v-icon>
          </a>

        </div>
      </div>
    </div>
    <v-container>
      <v-card dark class="text-center pa-5">
        <v-layout row wrap>
          <v-flex xs12 sm4>
            <v-btn depressed block @click="loadComponent = 'Introduction'">About me</v-btn>
          </v-flex>
          <v-flex xs12 sm4>
            <v-btn depressed block @click="loadComponent = 'Skills'">Skills</v-btn>
          </v-flex>
          <v-flex xs12 sm4>
            <v-btn depressed block @click="loadComponent = 'Education'">Education</v-btn>
          </v-flex>
        </v-layout>
        <transition name="slide-in" mode="out-in">
          <component :is="loadComponent"></component>
        </transition>
      </v-card>
    </v-container>
  </div>
</template>

<script>
import Introduction from '../components/Introduction'
import Skills from '../components/Skills'
import Education from '../components/Education'
export default {
  name: 'Home',
  components: {
    Introduction,
    Skills,
    Education
  },
  data () {
    return {
      loadComponent: 'Introduction',
      display: true,
    }
  }
}
</script>
<style scoped>
  .image-container {
    width: 100%;
    margin: auto;
    text-align: center;
  }
  .round {
    border-radius: 50%;
  }
   
  .slide-in-enter-active {
    animation: slideInOne 200ms ease-out forwards;
  }
  .slide-in-leave-active {
    animation: slideOut 200ms ease-out forwards;
  }
  .github-linkedin {
    animation: slideInOne 2s ease-out;
  }
  .twitter-email {
    animation: slideInTwo 2s ease-out;
  }
  @keyframes slideInOne {
    from {
      opacity: 0;
      transform: translateX(-100px);
    }
    to {
      opacity: 1;
      transform: translateX(0px);
    }
  }
  @keyframes slideInTwo {
    from {
      opacity: 0;
      transform: translateX(100px);
    }
    to {
      opacity: 1;
      transform: translateX(0px);
    }
  }
  @keyframes slideOut {
    from {
      opacity: 1;
      transform: translateX(0px);
    }
    to {
      opacity: 0;
      transform: translateX(-100px);
    }
  }


</style>
