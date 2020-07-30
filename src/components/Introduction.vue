<template>
  <div class="introduction">
    <div class="py-3">
      My name is <span class="title">Timothy Okooboh</span> and I am a full-stack software developer.
    </div>
    
    <div class="py-3">In simple terms, we could say that I have the skills, experience and capabilities to either work alone or work with a team in building innovative digital solutions by using web based technologies. </div>
    
    <div class="my-3">
      I create professional websites and web applications for small, medium and large scale businesses.
    </div>

    <div>
      What thrills me the most about the work I do are the solutions I provide with the codes I write.
    </div>
    <div class="my-3">
      PS: I'm also a Pharmacist 
      <v-icon>mdi-emoticon-cool-outline</v-icon>
    </div>

  </div>
</template>
<style>
  .introduction {
    width: 90%;
    margin: auto;
  }

  .star {
    position: relative;
    animation: star 3s ease-in infinite;
  }

  @keyframes star {
    0%{
      bottom: 0;
    }
    50%{
      bottom: 5px;
      left: 4px;
    }
    100%{
      bottom: 10px;
    }
  }
</style>