<template>
  <Header />
  <router-view></router-view>>
  <GameList :games=games />
</template>

<script>
import Header from "./components/Header.vue";
import GameList from "./components/GameList.vue";

export default {
  name: "App",
  components: {
    Header,
    GameList
  },
  methods: {
    async fetchGames() {
      const res = await fetch('http://localhost:8081/games')
      const data = await res.json();
        
      return data;
    }
  },
  data() {
    return {
      games: []
    }
  },
  async created() {
    this.games = await this.fetchGames();
  }
};
</script>

<style lang="scss">
  * {
    padding: 0;
    margin: 0;
    font-family: sans-serif;
}

body {
    background-image: url(https://wallpaper.dog/large/10936821.jpg);
}

</style>
