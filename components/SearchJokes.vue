<template>
  <div>
    <form action="." @submit.prevent="onSubmit">
      <input v-model="text" type="text" placeholder="Search Jokes..." />
      <input v-model="text" type="submit" value="Search" />
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: '',
    }
  },
  methods: {
    onSubmit() {
      this.$emit('search-text', this.text)
    },
  },
}
// $emit sends data to the parent component
</script>

<style></style>
