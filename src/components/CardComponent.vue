<template>
    <div class="col-12 col-sm-6 col-md-4 col-lg-3">
        <div class="character text-center">
            <img :src="character.card_images[0].image_url" :alt="character.name">
            <h4>{{ character.name }}</h4>
            <p>{{ character.archetype }}</p>
        </div>
    </div>
</template>

<script>
    export default{
        name: 'CardComponent',
        props: ['character']
    }
</script>


<style lang="scss" scoped>
    @use '../assets/styles/partials/variables' as *; 
    .character{
        background-color: $bg-color;
        min-height: 500px;
        min-width: 300px;
    }
    h4 {
        text-transform: capitalize;
        color: white;
        font-size: 20px;
    }
    img {
        box-shadow: 0 0 6px 3px rgba(#000, 0.15);
        width: 270px;
        margin-top: 15px;
    }
</style>
