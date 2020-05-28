<template>
  <div>
    <v-container>
      <h1 class="text-center pt-5">These are my works</h1>
      <v-card flat>
        <v-layout row>

          <v-flex xs12 sm6 md6 lg4 class="my-2 pa-5 load-lazy " v-for="(project, index) in projects" :key="index">
            <div>
              <v-btn text class="title"><a :href ="project.url" target="_blank" style="text-decoration: none; letter-spacing: 1.08px">{{project.name}}</a></v-btn>
            </div>

            <div class=" my-5">
              <a :href="project.url" target="_blank" style="text-decoration:none"> 
                <v-icon @click="visitWebpage" class="mx-5">mdi-web</v-icon>
              </a>
              <a :href="project.githubRepo" target="_blank" style="text-decoration:none"> 
              <v-icon @click="visitGithub">mdi-github</v-icon>
              </a>
            </div>

            <div>
              <v-img :src="project.image"></v-img>
            </div>

            <div class="my-5"> 
              {{project.description}}
            </div>

          </v-flex>

        </v-layout>
      </v-card>
    </v-container>
  </div>
</template>
<script>
  export default {
    data () {
      return {
        projects: [
          {
            name: 'INSPIRATIONS', 
            url: "https://findinspirations.info/", 
            githubRepo: 'https://github.com/timothyokooboh/inspirations', 
            image: "/inspire.png", 
            urlIcon: 'mdi-web', 
            githubIcon: 'mdi-github',
            description: 'A progressive web app where users can create, share and find inspirational stories'
          },
          {
            name: 'COVID-19 DASHBOARD', 
            url: "https://timothyokooboh.github.io/#/", 
            githubRepo: 'https://github.com/timothyokooboh/covid19-dev', 
            image: "/covid.png", 
            urlIcon: 'mdi-web', 
            githubIcon: 'mdi-github',
            description: 'A single page application that displays coronavirus statistics for different countries based on data from WHO'
          },
          {
            name: 'DICTIONARY', 
            url: "https://timothyokooboh.github.io/dictionary/#/", 
            githubRepo: 'https://github.com/timothyokooboh/dictionary-dev', 
            image: "/dict.png", 
            urlIcon: 'mdi-web', 
            githubIcon: 'mdi-github',
            description: 'A progressive web app that uses the owlbot.js NPM package to display the meaning of English words'
          },
        ]
      }
    },

    mounted (){
      const loadLazy = document.querySelectorAll('.load-lazy')
      const observer = new IntersectionObserver((entries) => {
        entries.forEach((entry)=>{
          if(entry.isIntersecting){
            entry.target.style.animation="animate 500ms ease-out forwards"
          }else{
            entry.target.style.animation="none"
          }
        })
      });
      loadLazy.forEach((loadItem)=>{
         observer.observe(loadItem)
      })
    }
  }
</script>
<style>
  @keyframes animate {
    from{
      opacity: 0;
      transform: translateY(-100px);
    }
    to{
      opacity: 1;
      transform: translateY(0px);
    }
  }
</style>
