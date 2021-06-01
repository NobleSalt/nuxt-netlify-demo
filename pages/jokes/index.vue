<template>
  <div class="jokes">
    <SearchJokes @search-text="Search" />
    Jokes
    <h4>name: {{ name }}</h4>
    <br />
    <Joke v-for="(joke, index) in jokes.results" :key="index" :joke="joke" />
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      name: '',
      jokes: 'Jok',
    }
  },
  head() {
    return {
      title: 'upshoot | Jokes',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Best place for  corny dad jokes',
        },
      ],
    }
  },
  async created() {
    const config = {
      headers: {
        Accept: 'application/json',
      },
    }
    // try {
    const res = await axios.get('https://icanhazdadjoke.com/search', config)
    this.jokes = res.data
    // console.log(res.data)
    // } catch (error) {
    // console.log(error)
    // }
  },
  methods: {
    Search(value) {
      this.name = value
    },
  },
}
</script>

<style>
.jokes {
  padding: 0.5rem;
  margin: 0.5rem 1rem;
}
</style>
