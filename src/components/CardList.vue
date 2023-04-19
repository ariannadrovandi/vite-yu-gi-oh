<template>
    <section class="main-bg container mt-4">
        <div class="row">
            <div class="col-12  text-center">
              <div class="bg-dark fw-bold text-white mt-3 py-3">Cards</div>
          </div>
        </div>
        <div class="row row-cols-1 row-cols-sm-2 row-cols-md-4 row-cols-lg-6 gy-2 my-2 justify-content-center  ">
            <CardComponent v-for="(character, index) in store.characterList" :key="index" :character="character" />
        </div>
    </section>
</template>

<script>
    import { store } from '../data/store';
    import CardComponent from './CardComponent.vue';
    export default{
        name: 'CardList',
        components: {
            CardComponent,
        },
        data() {
            return {
                store,
            }
        },
            methods: {
        }
    }
</script>


<style lang="scss" scoped>
    @use '../assets/styles/partials/variables' as *;
    .main-bg{
        background-color: $light-bg;
    }
</style>