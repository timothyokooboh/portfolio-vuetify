<template>
    <v-container>
      <h1 class="text-center py-5">Have a project idea? <br>Let's have a conversation</h1>
      <v-card dark flat>
        <v-layout wrap row class="my-5">
          <v-flex>
            <v-btn text class="my-5 mx-3">
              <v-icon large left>mdi-phone</v-icon>
              <span class="subheading font-weight-bold"> <a href="tel:+2348176581327" style="text-decoration: none; color: #FFF">">+2348176581327</a></span>
            </v-btn>
          </v-flex>
          <v-flex>
            <v-btn text class="my-5 mx-3">
              <v-icon large left>mdi-email</v-icon>
              <span class="subheading font-weight-bold"> <a href="mailto:okoobohtimothy@gmail.com?subject=Let's have a conversation" style="text-decoration:none; color: #FFF">okoobohtimothy@gmail.com</a></span>
            </v-btn>
          </v-flex>
          <v-flex>
            <v-btn text class="my-5 mx-3">
              <v-icon large left>mdi-google-maps</v-icon>
              <span class="subheading font-weight-bold"> Lagos, Nigeria</span>
            </v-btn>
          </v-flex>
        </v-layout>
        <v-footer class="py-5">
          <v-layout>
            <v-flex >
              <v-btn text>
                <a href="https://github.com/timothyokooboh" ref="github" target="_blank"></a>
                <v-icon large left @click="github">
                  mdi-github
                </v-icon>
              </v-btn>
            </v-flex>
            <v-flex>
              <v-btn text>
              <a href="https://twitter.com/inspiretim24" ref="twitter" target=_blank></a>
              <v-icon large left @click="twitter"> mdi-twitter </v-icon>
              </v-btn>
            </v-flex>
            <v-flex>
              <v-btn text>
                <a href="https://linkedin.com/in/timothy-okooboh-193980165/" ref="linkedin" target="_blank"></a>
                <v-icon large left @click="linkedin">mdi-linkedin</v-icon>
              </v-btn>
            </v-flex>
          </v-layout>
        </v-footer>
      </v-card>
    </v-container>
</template>
<script>
export default {
  methods: {
    github () {
      this.$refs.github.click()
    },
    twitter () {
      this.$refs.twitter.click()
    },
    linkedin () {
      this.$refs.linkedin.click()
    }
  }
}
</script>