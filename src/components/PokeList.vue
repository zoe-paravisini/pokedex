<!-- TEMPLATE -->
<template>
    <div class="pokecard">
        <PokeCard v-for="pokemon of pokemons" :key="pokemon" :pokemon="pokemon">
        </PokeCard>;

    </div>
</template>

<!-- SCRIPT -->
<script>
    import PokeCard from './PokeCard.vue'
    import json_pokemons from '@/pokemon.json'

    export default {
        name: 'PokeList',
        components: {
            PokeCard
        },
        data() {
            return {
                
                pokemons : json_pokemons,
            }
        }
    }
</script>

<style scoped>
.pokecard{
    display: grid;
    grid-template-columns: repeat(3, 1fr);

}
</style>