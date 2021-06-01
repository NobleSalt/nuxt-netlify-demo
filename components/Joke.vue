<template>
  <div class="joke">
    <a :href="`/jokes/${joke.id}`">
      <p>{{ joke.joke }}</p>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    joke: { type: [String, Object], default: 'Joke' },
    id: { type: [String, Object], default: 'Joke' },
  },
}
</script>

<style>
.joke {
  padding: 0.5rem;
  border: 1px dotted #ccc;
  margin: 0.5rem 0;
}
</style>
