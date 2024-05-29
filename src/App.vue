<script>
import AppHeader from './components/AppHeader.vue'
import Main from './components/Main.vue'
import CardList from './components/CardList.vue'
import axios from 'axios'

export default {

  components: {
    AppHeader, Main, CardList,
  },
  
 

  data() {
    return {
      carte: []
    }
  },


  methods: {
  },


  mounted() {
    axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=4&offset=0").then((response) => {
      console.log(response.data.data);
      this.carte = response.data.data;
    }).catch((error) => {
      console.log(error)
    });
  },
}
</script>

<template>
  <AppHeader />
  <Main :carte="carte"/>
  <CardList  />
</template>

<style></style>



<!--
<template>
  <AppHeader />
  <Main :cards="cards" />
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import Main from './components/Main.vue'
import CardList from './components/CardList.vue'
import axios from 'axios'

export default {
  components: {
    AppHeader, Main, CardList,
  },
  
  data() {
    return {
      cards: []
    }
  },

  mounted() {
    axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0").then((response) => {
      console.log(response.data.data);
      this.cards = response.data.data;
    }).catch((error) => {
      console.log(error)
    });
  },
}
</script>

<style>
</style>

-->

