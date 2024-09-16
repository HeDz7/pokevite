<script setup>
const pokemon = defineProps(["name", "urlBaseSvg"])
</script>

<template>
  <div class="section col-4">
    <div class="card mb-3 p-2">
        <p class="text-center">{{pokemon.name}}</p>
        <img :src="urlBaseSvg" class="card-img-top" alt="" height="80">
    </div>
  </div>
</template>

<style scoped>
.card {
    background-color: bisque;
    cursor: pointer;
    transition: .2s ease-in-out;
}

.card:hover {
    background-color: aliceblue;
}

.card p {
    text-transform: capitalize;
    font-weight: 600;
}

</style>