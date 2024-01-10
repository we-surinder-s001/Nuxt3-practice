<template>
  <header class="shadow-sm bg-white">
    <nav class="container mx-auto flex justify-between p-4">
      <div class="font-bold">NUXT 3</div>
      <ul class="flex gap-4 items-center">
        <Nuxt-link to="/">
          <li>Home</li>
        </Nuxt-link>
        <Nuxt-link to="/about">
          <li>About</li>
        </Nuxt-link>
        <Nuxt-link to="/products">
          <li>Products</li>
        </Nuxt-link>
        <Nuxt-link to="/products/30" class="btn">
          <li>Product-30</li>
        </Nuxt-link>
      </ul>
    </nav>
  </header>

  <h1>Products Layout</h1>
  <div class="container mx-auto px-4 my-10">
    <slot/>
  </div>

  <footer class="border-t-2">
    <ul class="flex gap-4 container mx-auto px-4">
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
</style>