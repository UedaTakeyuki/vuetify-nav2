<template>
  <v-app>
    <!-- Navigation bar -->
    <Navbar titleStr="Demo App" :links="links"/>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
/* eslint-disable */
import {Navbar} from '../../src/build-entry'
//import {Navbar} from '../../dist/VuetifyNav2.umd'
import { mdiHome, /*mdiArrowLeft*/} from "@mdi/js";
import SvgIconMenu from './components/SvgIconMenu.vue'

export default {
  components: { Navbar, SvgIconMenu},
  data: () => ({
    links: [
      { icon: mdiHome, text: 'Home', route: '/'},
      { icon: '', text: 'About', route: '/about', svg: SvgIconMenu},
    ]
  }),
  mounted(){
    console.log("links",this.links)
  }
}
</script>