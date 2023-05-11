<script setup>
const pokemon = defineProps (["name", "xp", "height", "img"])
</script>

<template>
  <div class="card CardPokemonSelected">
    <img
      :src="pokemon.img"
      height="250"
      class="card-img-top pt-2"
      :alt="pokemon.name"
    />
    <div class="card-body">
      <h5 class="card-title text-center">{{ pokemon.name }}</h5>
      <hr />
      <div class="row">
        <section class="col">
          <strong>XP: </strong>
          <span> {{ pokemon.xp }}</span>
        </section>

        <section class="col">
          <strong>Altura: </strong>
          <span> {{ pokemon.height }}</span>
        </section>
      </div>
    </div>
  </div>
</template>

<style scoped>
.CardPokemonSelected {
    height: 450px;
    background: rgb(72,63,251);
    background: radial-gradient(circle,rgba(220,197,106,0.6) 0%,rgba(244,0,0,0.3) 100%);
}

</style>
