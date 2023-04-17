<template>
  <HeaderComponent/>
  <main>
    <select name="" id="">select</select>
    <CardList/>
  </main>
</template>

<script>
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
      
    }
  },
  methods: {
    
  },
  mounted() {
    
  }
}
</script>

<style lang="scss" scoped>
  
</style>
