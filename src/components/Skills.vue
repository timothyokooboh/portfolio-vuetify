<template>
  <div>
    <div class="mb-5">
      <div class="title my-3">Front-end languages</div>
      <div class="flex-logos">
        <div><img src="html_logo.png" alt="html logo"></div>
        <div><img src="css_logo.png" alt="css logo"></div>
        <div><img src="js_logo.png" alt="javascript logo"></div>
        <div><img src="typescript_logo.png" alt="typescript logo"></div>
      </div>
    </div>

    <div class="mb-5">
      <div class="title">Front-end frameworks</div>
      <div class="flex-logos">
        <div><img src="vuejs_logo.jpeg" alt="vue.js logo"></div>
        <div><img src="nuxtjs_logo.jpg" alt="nuxt.js logo"></div>
        <div><img src="chartjs_logo.png" alt="chart.js logo"></div>
        <div><img src="bootstrap_logo.png" alt="bootstrap logo"></div>
        <div><img src="sass_logo.png" alt="sass logo"></div>
      </div>
    </div>

    <div class="mb-5">
      <div class="title">Server-side techonologies </div>
      <div class="flex-logos">
        <div><img src="nodejs_logo.png" alt="node.js logo"></div>
        <div><img src="expressjs_logo.png" alt="express.js logo"></div>
        <div><img src="laravel_logo.png" alt="laravel logo"></div>
      </div>
    </div>

    <div class="mb-5">
      <div class="title">Server-side database</div>
      <div class="flex-logos">
        <div><img src="mongo_logo.png" alt="mongodb logo"></div>
        <div><img src="mysql_logo.png" alt="mysql logo"></div>
      </div>
    </div>

    <div class="mb-5">
      <div class="title">Version control</div>
      <div class="flex-logos">
        <div><img src="git_logo.png" alt="git logo"></div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .flex-logos {
    display: flex;
    flex-wrap: wrap;
    justify-items: center;
    justify-content: center;
  }
  .flex-logos div {
    margin: 10px;
  }
  .flex-logos img {
    width: 120px;
    height: 100px;
    object-fit: contain;
  }
</style>