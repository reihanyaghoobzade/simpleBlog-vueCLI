<template>
  <header>
    <nav class="bg-gray-100 border-gray-200 px-4 py-4 rounded">
      <div class="container flex justify-strat items-center gap-12 md:gap-20 mx-auto">
        <h1 class="text-2xl font-semibold" to="/">Vue.js</h1>
        <div class="flex justify-center items-center">
          <div class="flex flex-row space-x-8 mt-0 font-medium">
              <router-link to="/" class="block text-gray-500 p-0 cursor-pointer">Home</router-link>
              <router-link to="/users" class="block text-gray-500 p-0 cursor-pointer">Users</router-link>
              <router-link to="/posts" class="block text-gray-500 p-0 cursor-pointer">Posts</router-link>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {

}
</script>

<style scoped>
.router-link-active {
  @apply text-blue-700 !important;
}

</style>