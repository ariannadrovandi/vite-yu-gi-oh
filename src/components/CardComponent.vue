<template>
    <div class="col-12 col-sm-6 col-md-4 col-lg-3">
        <div class="character text-center">
            <img :src="character.image_url" :alt="character.name">
            <h4>{{ character.name }}</h4>
            <div>{{ character.desc }}</div>
            <div class="font-weight-bold">{{ character.archetype }}</div>
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
    h4 {
        text-transform: capitalize;
    }
    img {
        border-radius: 50%;
        box-shadow: 0 0 6px 3px rgba(#000, 0.15);
    }
</style>
