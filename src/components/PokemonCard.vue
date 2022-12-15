<script setup lang="ts">
import type { IPokemon } from '@/interfaces/Pokemon.interface';

interface ComponentProps {
  pokemon?: IPokemon | null,
  error?: Error
}

defineProps<ComponentProps>();
</script>

<template>
  <div className="pokemon-card">
    <section>
      <!-- Pokemon name with h3 tag -->
      <img loading="lazy" className="pokemon-sprite" />
      <article className="pokemon-data">
        <details>
          <summary>ID</summary>
          <!-- Pokemon id with p tag -->
        </details>
        <details>
          <summary>Types</summary>
          <!-- Pokemon types with a tags -->
        </details>
        <details>
          <summary>Abilities</summary>
          <!-- Pokemon abilities with a tags -->
        </details>
        <details>
          <summary>Moves</summary>
          <!-- Pokemon moves with a tags -->
        </details>
      </article>
    </section>
    
    <!-- Show error on h3 text. -->
    <h3 className="pokemon-error">ERROR: </h3>
  </div>
</template>

<style scoped>
.pokemon-card {
  display: flex;
  flex-flow: column;
  border: 1px solid gray;
  border-radius: 8px;
  padding: 16px;
  margin-top: 16px;
}

.pokemon-data details {
  margin-top: 16px;
  display: flex;
  flex-flow: column;
  gap: 8px;
}

.pokemon-sprite {
  width: 128px;
  height: 128px;
}

.pokemon-error {
  color: red;
}
</style>
