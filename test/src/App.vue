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

export default {
  components: { Navbar},
  data: () => ({
    links: [
      { icon: mdiHome, text: 'Home', route: '/'},
      { icon: '', text: 'About', route: '/about'},
    ]
  }),
  mounted(){
    console.log("links",this.links)
  }
}
</script>