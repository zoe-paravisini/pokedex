<!-- TEMPLATE -->
<template>
    <div class="template">
    <div class="card">
        <img center class="image" :src='imgpath'>
        {{pokemon.name}}
    <!-- <ButtonInfosOnHover> Ajouter au deck </ButtonInfosOnHover> -->
    </div>
</div>
</template>

<!-- SCRIPT -->
<script>
// import ButtonInfosOnHover from './ButtonInfosOnHover.vue'


    export default {
            props: {
                pokemon: {
                    type: Object
                },
                
            },
// components: {
//                     ButtonInfosOnHover
//         },
        computed: {
            imgpath(){
                return "/images/"+this.pokemon.name.toLowerCase()+".png"
            }
        }
    }

</script>

<!-- CSS -->
<style scoped>
.template{
    display: flex;
    justify-content: center;
}

.card{
    margin: 40px;
    padding:50px;
     border-radius: 5px;
     background-color: rgba(210,10,240,0.5);
}
.image{
    display: block;
}
</style>