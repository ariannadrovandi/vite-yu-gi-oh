<template>
  <HeaderComponent/>
  <main class="container mt-4 mb-4">
    <SelectComponent @search-change="getCards"/>
    <CardList/>
  </main>
</template>

<script>
  import { store } from './data/store';
  import axios from 'axios';
  import HeaderComponent from './components/HeaderComponent.vue';
  import SelectComponent from './components/SelectComponent.vue';
  import CardList from './components/CardList.vue';
  export default {
    name: 'App',
    components: {
      HeaderComponent,
      SelectComponent,
      CardList,
    },
    data() {
      return {
        store
      }
    },
    methods: {
      getCards() {
        const url = store.baseUrl + store.endpoint;

        let params = {}
        for (let key in store.search) {
          if (store.search[key]) {
            params[key] = store.search[key]
          }
        }

        if (store.search.archetype != ''){
          url = 'https://db.ygoprodeck.com/api/v7/cardinfo.php?'
          console.log(url)
        }

        axios.get(url).then((res) => {
          store.characterList = res.data.data;
        });
      }
    },
    mounted() {
      this.getCards();
    }
  }
</script>

<style lang="scss" scoped>
  
</style>
