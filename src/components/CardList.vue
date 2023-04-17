<template>
    <section class="main-bg container mt-4">
        <p>ciao</p>
        <div class="row">
            <p>ciao</p>
            <CardComponent v-for="(character, index) in store.characterList" :key="character.id" :character="character" />
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
                store
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
        .row{
            border: 1px solid black;
        }
    }
</style>