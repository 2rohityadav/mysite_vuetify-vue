<template>
  <div class="hello">

  <v-app id="example-8" dark>
    <!-- navigation drawer -->
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="mini"
      dark
    >
      <v-list class="pa-0">
        <v-list-tile v-if="mini" @click.native.stop="mini = !mini">
          <v-list-tile-action>
            <v-icon>chevron_right</v-icon>
          </v-list-tile-action>
        </v-list-tile>
        <v-list-tile avatar tag="div">
          <v-list-tile-avatar>
            <img src="../assets/avatar-ninja.png" />
          </v-list-tile-avatar>
          <v-list-tile-content>
            <v-list-tile-title>Rohit Yadav</v-list-tile-title>
          </v-list-tile-content>
          <v-list-tile-action>
            <v-btn icon @click.native.stop="mini = !mini">
              <v-icon light>chevron_left</v-icon>
            </v-btn>
          </v-list-tile-action>
        </v-list-tile>
      </v-list>
      <v-list class="pt-0" dense>
        <v-divider></v-divider>
        <v-list-tile v-for="item in items" :key="item.title">
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <!--End navigation drawer -->
    <!-- toolbar -->
    <v-toolbar fixed dark>
      <v-toolbar-side-icon @click.native.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>Toolbar</v-toolbar-title>
    </v-toolbar>
    <!-- start main content -->
    <main>
      <main-content></main-content>
    </main>
    <!-- end main content -->
    <app-footer></app-footer>
  </v-app>
  </div>
</template>

<script>
import MainContent from './MainContent.vue'
import Footer from './Footer.vue'

export default {
  components: {
    mainContent: MainContent,
    appFooter: Footer
  },
  data () {
    return {
      drawer: null,
      items: [
        { title: 'Home', icon: 'dashboard' },
        { title: 'About', icon: 'question_answer' }
      ],
      mini: false,
      right: null
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body{
  font-family: 'Coustard', serif;
}
.hello {
  display: flex;
  flex-direction: column;
}
  #example-8 .card {
    background: #424242
  }

.navigation-drawer {
  background: #000;
}
</style>
