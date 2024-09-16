<script setup>
const pokemon = defineProps(["name", "xp", "height", "img"]);
</script>

<template>
  <div class="card">
    <img
      v-if="pokemon.name"
      :src="pokemon.img"
      class="card-img-top pt-2"
      alt="..."
      height="250"
    />
    <img
      v-else
      src="../assets/egg_pokemon.svg"
      class="card-img-top pt-2"
      alt="???"
      height="250"
    />
    <div class="card-body">
      <h5 class="card-title text-center">{{ pokemon.name || "???" }}</h5>
      <hr />
      <div class="row">
        <div class="col-6 text-center">
          <strong> XP: </strong>
          <span> {{ pokemon.xp }} </span>
        </div>
        <div class="col-6 text-center">
          <strong> Height: </strong>
          <span> {{ pokemon.height }} </span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card {
  height: 700px;
}

.card-img-top {
  height: 60%;
}
</style>
