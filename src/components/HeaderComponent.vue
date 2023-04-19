<template>
    <div id="header" class="p-3 d-flex align-items-center justify-content-start">
        <h1 class="ms-2">YU-GI-OH API</h1>
    </div>
</template>

<script>
    export default{
        name: 'HeaderComponent'
    }
</script>


<style lang="scss" scoped>
    @use '../assets/styles/partials/variables' as *;
    #header{
        height: 80px;
        width: 100%;
        background-color: $light-bg ;
        h1{
            font-size: 1.7rem;
        }
    }
</style>