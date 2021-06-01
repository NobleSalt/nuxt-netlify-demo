<template>
  <div class="container">
    <div>
      <h1 class="title">shoot</h1>
    </div>
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
      title: 'upshoot | Home',
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
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
