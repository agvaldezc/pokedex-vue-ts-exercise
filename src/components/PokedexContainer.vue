<script setup lang="ts"></script>

<template>
  <section className="pokedex">
    <form className="pokedex-search-form">
      <h2>Pokedex Component</h2>
      <fieldset>
        <input name="query" type="text" placeholder="Pokemon name or ID" />
        <button type="submit">Search Pokemon</button>
      </fieldset>
    </form>
    <article className="pokedex-container">
      <!-- Need to use the PokemonCard component. -->
    </article>
  </section>
</template>

<style scoped>
fieldset {
  border: none;
}

.pokedex {
  display: flex;
  flex-flow: column;
}

.pokedex-search-form {
  display: flex;
  flex-flow: column;
  gap: 16px;
}
</style>