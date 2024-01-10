<template>
  <header>
    <ul class="flex">
      <Nuxt-link to="/">
        <li>Home</li>
      </Nuxt-link>
      <Nuxt-link to="/about">
        <li>About</li>
      </Nuxt-link>
      <Nuxt-link to="/products">
        <li>Products</li>
      </Nuxt-link>
      <Nuxt-link to="/products/30">
        <li>Product-30</li>
      </Nuxt-link>
    </ul>
  </header>

  <h1>
    this is products layout
  </h1>

  <slot/>

  <footer>
    <ul class="flex">
      <Nuxt-link to="/">
        <li>Home</li>
      </Nuxt-link>
      <Nuxt-link to="/about">
        <li>About</li>
      </Nuxt-link>
      <Nuxt-link to="/products">
        <li>Products</li>
      </Nuxt-link>
      <Nuxt-link to="/products/30">
        <li>Product-30</li>
      </Nuxt-link>
    </ul>
  </footer>
</template>

<style scoped>
.router-link-exact-active {
  color: lightgreen;
}

.flex {
  display: flex;
  gap: 2rem;
  list-style: none;
}

.flex * {
  text-decoration: none;
}
</style>