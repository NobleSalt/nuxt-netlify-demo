<template>
  <div class="id">
    <h4>Name: {{ $route.params.id }}</h4>
    <img :src="`https://icanhazdadjoke.com/j/${$route.params.id}.png`" alt="" />
    <hr />
    <small>Joke ID: {{ $route.params.id }}</small>
  </div>
</template>

<script>
// import axios from 'axios'

export default {
  data() {
    return {
      src: '',
    }
  },
  head() {
    return {
      title: 'upshoot | ' + this.$route.params.id,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Best place for  corny dad jokes',
        },
      ],
    }
  },
}
</script>

<style>
.id {
  padding: 1rem;
  padding-right: 0;
  border: 1px dotted #ccc;
  margin: 1rem 2rem;
}
</style>
