<template>
  <v-app>
    <v-toolbar
      app
      :clipped-left="clipped"
    >
      <v-toolbar-title v-text="title"></v-toolbar-title>
                    <v-avatar
            :tile="tile"
            :size="avatarSize"
            color="grey lighten-4"
      >
        <img class="circular" src="@/assets/BitEmojiProfilePic.png" alt="avatar">
      </v-avatar>
    </v-toolbar>
    <v-content>
      <HelloWorld/>
    </v-content>
    <v-navigation-drawer
      temporary
      :right="right"
      v-model="rightDrawer"
      fixed
      app
    >
      <v-list>
        <v-list-tile>
          <v-list-tile-title>Projects</v-list-tile-title>
        </v-list-tile>
        <v-list-tile @click="greet">
          <v-list-tile-action>
            <v-icon>music_note</v-icon>
          </v-list-tile-action>
          <v-list-tile-title>Pedal-Pi</v-list-tile-title>
        </v-list-tile>
        <v-list-tile @click="right = !right">
          <v-list-tile-action>
            <v-icon>compare_arrows</v-icon>
          </v-list-tile-action>
          <v-list-tile-title>Switch drawer (click me)</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-footer :fixed="fixed" app>
      <span>&copy; 2018</span>
    </v-footer>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data () {
    return {
      clipped: false,
      drawer: true,
      fixed: false,
      items: [{
      }],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Robin Listerberg'
    }
  },

  computed: {
      avatarSize () {
        return `50px`
      }
  },
  methods: {
    greet: function (event) {
        alert('Hello' + this.name + '!')

        if(event){
            alert(event.target.tagName)
        }
    }
  }
}
</script>
<style>
.circular{
  width: 70px;
  height: 70px;
  background-size: cover;
  border-radius: 50px;
  -webkit-border-radius: 50px;
  -moz-border-radius: 50px;
}
</style>