<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
<!--      <HelloWorld/>-->
    <div class="container">
      <div class="row">
        <Card :alumno="alumno" v-for="(alumno,index) in alumnos" :key="index"></Card>
      </div>
    </div>
    </v-main>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld';
import Card from './components/Card'
export default {
  name: 'App',

  components: {
    // HelloWorld,
    Card
  },

  data: () => ({
    alumnos:[
      {nombre:'JUanito alberto',curso:'1B',imagen:'https://www.questionpro.com/blog/wp-content/uploads/2018/08/Encuestas-estudiantes.jpg'},
      {nombre:'Ana alberto',curso:'3B',imagen:'https://cdn.aarp.net/content/dam/aarp/politics/events-and-history/2016/07/1140-are-you-smarter-than-8th-grader-quiz-esp.imgcache.rev.web.900.513.jpg'},
      {nombre:'febiola alberto',curso:'4B',imagen: 'https://cognosonline.com/wp-content/uploads/2020/04/Razones-por-las-que-las-plataformas-online-aumentan-la-motivacio%CC%81n-de-los-estudiantes.png'},
      {nombre:'alberto alberto',curso:'2B',imagen:'https://www.questionpro.com/blog/wp-content/uploads/2018/08/Encuestas-estudiantes.jpg'},
      {nombre:'mario alberto',curso:'2B',imagen: 'https://cognosonline.com/wp-content/uploads/2020/04/Razones-por-las-que-las-plataformas-online-aumentan-la-motivacio%CC%81n-de-los-estudiantes.png'},
      {nombre:'jesusu alberto',curso:'1B',imagen:'https://www.questionpro.com/blog/wp-content/uploads/2018/08/Encuestas-estudiantes.jpg'},
      {nombre:'jesusu alberto',curso:'1B',imagen:'https://cdn.aarp.net/content/dam/aarp/politics/events-and-history/2016/07/1140-are-you-smarter-than-8th-grader-quiz-esp.imgcache.rev.web.900.513.jpg'},
    ]
  }),
};
</script>
