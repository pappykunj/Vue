<template>
  <v-app>
    <v-main>
      <MyHome/>
      <MyBanner/>
      <SectionOne/>
    </v-main>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld';
import MyHome from './components/HomeMe';
import MyBanner from './components/MyBanner';
import SectionOne from './components/SectionOne';
import './assets/sytes/style.css';
import './assets/sytes/font.css';


export default {
  name: 'App',

  components: {
    // HelloWorld,
    MyHome,
    MyBanner,
    SectionOne
  },

  data: () => ({
    //
  }),
};
</script>
