<template>
    <section class="choice">
      <span class="bt" data-type="" @click="filter('')">Afficher tout le monde</span>
      <span class="bt bt--femme" data-type="" @click="filter('Female')">Afficher toutes les femmes</span>
      <span class="bt bt--homme" data-type="" @click="filter('Male')">Afficher tous les hommes</span>
    </section>
</template>

<script>
export default {
// propriétés passables à mon composant
    methods:{
        filter(type){
            this.$emit('filterRobots', type)
        }
    }
};
</script>

<style>

</style>
