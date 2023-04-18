<template>
  <HeaderComponent/>
  <main class="container mt-4 mb-4">
    <select name="type" id="type">
      <option value="select">select</option>
      <option value="alien">alien</option>
    </select>
    <CardList/>
  </main>
</template>

<script>
import { store } from './data/store';
import axios from 'axios';
import HeaderComponent from './components/HeaderComponent.vue';
import CardList from './components/CardList.vue';
export default {
  name: 'App',
  components: {
    HeaderComponent,
    CardList,
  },
  data() {
    return {
      store
    }
  },
  methods: {
    getCards() {
      const url = store.baseUrl;
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
