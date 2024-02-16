<template>
<div>
    <PokeCard @mouseenter="showMe = true" @mouseleave="showMe = false"/>
</div>
        <div v-if="showMe">

          <div> 
            <input type="button"/>
            {{ showMe }}
          </div>

            <div>
              <h4>Type(s)</h4>
                <span>{{ pokemon.classification }}</span>
              <h4>Taille</h4>
                <span>{{ pokemon.height_m }}</span>
              <h4>Poids</h4>
                <span>{{ pokemon.weight_kg }}</span>
            </div>

            <div>
              <h4>Attaque</h4>
                <span>{{ pokemon.attack }}</span>
              <h4>Défense</h4>
                <span>{{ pokemon.defense }}</span>
              <h4>Rapidité</h4>
                <span>{{ pokemon.speed }}</span>
            </div>

        </div>
        
</template>

<script>
import PokeCard from './PokeCard.vue'
import json_pokemons from '@/pokemon.json'

export default {
  data() {
    return {
      showMe: false, 
    };
  }
};

</script>

<!-- CSS -->
<style scoped>
/* 
input{
    background-color: brown;
    margin: 10px, 5pxs;
}

.hover-object {
  width: 100px;
  height: 50px;
  background-color: lightblue;
  display: flex;
  justify-content: center;
  align-items: center;
}

.tooltip {
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
  background-color: rgba(0, 0, 0, 0.8);
  color: white;
  padding: 5px;
  border-radius: 5px;
  display: none;
}

.hover-object:hover .tooltip {
  display: block;
} */
</style>
