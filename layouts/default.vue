<template>
  <header>
    <ul>
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

  <slot/>
</template>

<style scoped>
.router-link-exact-active {
  color: lightgreen;
}
</style>