<template>
  <div class="home">
    <h1 class="text-center my-5">About Me</h1>
    <v-container>
      <v-card class="text-center pa-5">
        <v-layout row wrap>
          <v-flex xs12 sm4>
            <v-btn depressed block @click="loadComponent = 'Introduction'">Introduction</v-btn>
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
  .slide-in-enter-active {
    animation: slideIn 200ms ease-out forwards;
  }
  .slide-in-leave-active {
    animation: slideOut 200ms ease-out forwards;
  }
  @keyframes slideIn {
    from {
      opacity: 0;
      transform: translateX(-100px);
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
