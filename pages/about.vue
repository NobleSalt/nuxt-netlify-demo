<template>
  <div>
    This is the About Page
    <h3>{{ name }}</h3>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Emmnauel',
    }
  },
  head() {
    return {
      title: 'upshoot | About',
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

<style lang="scss" scoped></style>
