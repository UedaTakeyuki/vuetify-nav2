<template>
  <v-app>
    <!-- Navigation bar -->
    <Navbar titleStr="Demo App" :links="links" qrExp=""/>
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
import SvgPikachu from './components/SvgPikachu.vue'
import SvgPikachu2 from './components/SvgPikachu2.vue'

export default {
  components: { Navbar, SvgIconMenu, SvgPikachu, SvgPikachu2},
  data: () => ({
    links: [
      { icon: mdiHome, text: 'Home', route: '/'},
      { icon: '', text: 'About', route: '/about', svg: SvgIconMenu},
      { icon: '', text: 'Pikachu', route: '/about', svg: SvgPikachu},
      { icon: '', text: 'Pikachu2', route: '/home', svg: SvgPikachu2},
    ]
  }),
  mounted(){
    console.log("links",this.links)
  }
}
</script>