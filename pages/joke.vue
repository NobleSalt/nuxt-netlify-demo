<template>
  <div>
    Jokes
    <h4>name: {{ name }}</h4>
    <br />
    <Joke
      v-for="(joke, index) in jokes.results"
      :key="index"
      :joke="joke.joke"
    />
    <!-- <ul>
      <a :href="joke.id">
        <li>{{ index + 1 }}. {{ joke.joke }}</li>
      </a>
      <br />
    </ul> -->
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      name: 'Emmnauel',
      jokes: [],
    }
  },
  head() {
    return {
      title: 'upshoot | Joke',
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
    try {
      const res = await axios.get(
        `https://icanhazdadjoke.com/j/${this.$route.params}`,
        config
      )
      this.jokes = res.data
      console.log(res.data)
    } catch (error) {}
  },
}
</script>

<style></style>
