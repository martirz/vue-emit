<template>
  <v-app>
    <v-content>
      <Reader />
      <PlayerControl :playIcon="this.playing ? 'pause' : 'play'" :playing=this.playing v-on:togglePlay="handleTogglePlay"/>
    </v-content>
  </v-app>
</template>

<script>
import PlayerControl from "./components/PlayerControl";
import Reader from "./components/Reader";

export default {
  name: "App",
  components: {
    PlayerControl,
    Reader
  },
  data: () => ({
    playing: false
  }),
  methods: {
    handleTogglePlay: function (playing) {
      this.playing = playing
    }
  }
};
</script>
