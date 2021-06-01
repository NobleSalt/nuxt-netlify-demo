<template>
  <div class="header head">
    <nuxt-link class="header_title" to="/">Dad Jokes</nuxt-link>
    <!-- <h3 class="header_title">Dad Jokes</h3> -->
    <ul class="header_links">
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/jokes">Jokes</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">About</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  flex-wrap: wrap;

  &_title {
    font-size: 2rem;
    cursor: pointer;
  }

  &_links {
    display: flex;
    // width: 60%;
    // justify-content: space-between;

    a {
      display: inline-block;
      background-color: darken(gray, 30);
      margin-right: 1rem;
      border-radius: 4px;
      padding: 5px 10px;
      color: white;
      cursor: pointer;
      transition: all 300ms ease-in-out;

      &:hover {
        color: black;
        background-color: gray;
        box-shadow: 0 2px 5px 2px black;
      }
    }
  }
}

@media screen and (max-width: 320px) {
  .header {
    align-items: center;
    flex-direction: column;
  }
}
</style>
