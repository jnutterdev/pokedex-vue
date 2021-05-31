<template>
    <div class="container">
        <h1>Pokemon</h1>
        <PokemonList :imageUrl="imageUrl" :apiUrl="apiUrl" />
    </div>
</template>

<script>
    import PokemonSearch from './PokemonSearch.vue';
    import PokemonList from './PokemonList.vue';
    import PokemonDetail from './PokemonDetail.vue';

    export default {
        data: () => {
            return {
                imageUrl: 'https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/',
                apiUrl: 'https://pokeapi.co/api/v2/pokemon',
            }
        },
        components: {
            PokemonSearch,
            PokemonList,
            PokemonDetail,
        }
    }
</script>

<style lang="scss" scoped>
    @import url('https://fonts.googleapis.com/css?family=Acme');

    .container {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        padding: 10px;
        width: calc(100% - 20px);
        min-height: calc(100vh - 20px);
        background: radial-gradient(#156f99, #0a2e50);

        font-family: 'Acme', arial;
        font-size: 1rem;
        font-weight: normal;
    }

    h1 {
        color: #efefef;
    }
</style>
