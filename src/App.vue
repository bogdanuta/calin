<template>
  <v-app>
    <Toolbar />
    <v-content>
    <v-container fluid>
      <router-view></router-view>
    </v-container>
  </v-content>
  </v-app>
</template>

<script>
import Toolbar from './components/Toolbar.vue'

export default {
  name: 'App',
  components: {
    Toolbar
  },
  data () {
    return {
      //
    }
  }
}
</script>
