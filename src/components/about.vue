<template>
  <v-row class="d-flex justify-center">
    <v-col class="d-flex justify-start flex-column mt-16" cols="5">
      <h1>Hi, There! <br>I am Otávio Gonçalves Lamberty</h1>
      <v-divider class="mr-3 mt-5 mb-5" :thickness="2" color="white"/>
      <h4 class="mt-5 pr-10 font-weight-regular" v-html="text"/>
    </v-col>
    <v-col  cols="5" class="d-flex justify-center align-center">
      <v-row class="elevation-10 pa-5 rounded-lg">
        <v-col class="d-flex flex-column" cols="3">
          <v-row>
            <v-col class="d-flex flex-column">
              <v-img
                src="../assets/images/annie.jpg"
                class="mb-5"
              />
              <v-img
                src="../assets/images/arya.jpg"
                class="mb-5"
              />
              <v-img
                src="../assets/images/jane.jpg"
              />
            </v-col>
          </v-row>
        </v-col>
        <v-col>
          <v-img
            src="../assets/images/profile.jpg"
            height="100%"
            cover
          />
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>

<script lang="ts">
export default {
  data() {
    return {
      text: '\nI\'m 23 yers old, and currently pursuing a degree in Computer Science at Federal University of Santa Maria (UFSM), Rio Grande do Sul, Brasil.<br>' +
        '\nMy desire to learn about technology and programming, especially about the foundations of computing, made me a very ambitious and hard workind person,' +
        '\n as i\'m always looking forward to improve my skills.' +
        '\nActually i\'m working at <a href="https://www.jetimob.com/" class="text-decoration-none" target="_blank">Jetimob<\a>,' +
        '\n as a Full Stack Web Developer, this jobs helped me improve, not only my programming skills, but also my social skills.<br>' +
        '\n<br>I started in the area in 2022 and i have experience with:' +
        '\nMongoDB, PostgreSQL, NodeJS, Laravel, Spring Boot, React, Vue, Flutter, Docker, Git, among others.' +
        '\nI enjoy studying about programming languages and developing new projects using these tools.' +
        '\n<br>My most used languages are Java/C, due to my major courses, and TypeScript, Dart and PHP due to my work.' +
        '\n<br><br><h2 class="pa-0">About me besides programming:</h2><br>' +
        'I like play some games with my friends, also sharing meals and drinks with them, i love spend time with my pets - you can say i\'m a cat lover :D' +
        '\nand you can see them in images left side - i also like enjoy view some series, like Game of Thrones, House of The Dragon, Arcane, The Last of Us...<br>' +
        '\nAn interesting fact about me is that when I was studying Electrical Engineering, I took a programming course and fell in love with the field.' +
        '\nThat\'s why I decided to change my major, and I started interning in app development right from the beginning.',
    }
  }
}
</script>

