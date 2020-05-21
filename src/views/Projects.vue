<template>
  <div>
    <v-container>
      <h1 class="text-center pt-5">These are my works</h1>
      <v-card flat>
        <v-layout row >
          <v-flex xs12 sm6 md6 lg4 class="my-2 pa-5 load-lazy ">
            <div>
              <v-btn text class="title"><a href ='https://findinspirations.info/' target="_blank" style="text-decoration: none; letter-spacing: 1.08px">INSPIRATIONS</a></v-btn>
            </div>
              <div>
                <v-img src='../images/laughter.jpg' width="300" height="300"></v-img>
              </div>
            <div class="my-5"> 
              A progressive web app where users can create, share and find inspirational stories
            </div>
          </v-flex>
          <v-flex xs12 sm6 md6 lg4 class="my-2 pa-5 load-lazy">
            <div>
              <v-btn text class="title"><a href ="https://timothyokooboh.github.io/#/" target="_blank" style="text-decoration: none; letter-spacing: 1.08px">COVID-19 DASHBOARD</a></v-btn>
            </div>
            <div>
              <v-img src='../images/corona.jpeg' width="300" height="300"></v-img>
            </div>
            <div class="my-5 ">
              A single page application that displays coronavirus statistics for different countries based on data from WHO
            </div>
          </v-flex>
          <v-flex xs12 sm6 md6 lg4 class="my-2 pa-5 load-lazy">
            <div>
              <v-btn text class="title"><a href="https://timothyokooboh.github.io/dictionary/#/" target="_blank" style="text-decoration: none; letter-spacing: 1.08px"> DICTIONARY </a> </v-btn>
            </div>
            <div>
              <v-img src='../images/dictionary.jpg' width="300" height="300"></v-img>
            </div>
            <div class="my-5 text-wrap" >
              A progressive web app that uses the owlbot.js NPM package to display the meaning of English words
            </div>
          </v-flex>
        </v-layout>
      </v-card>
    </v-container>
  </div>
</template>
<script>
  export default {
    mounted(){
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
