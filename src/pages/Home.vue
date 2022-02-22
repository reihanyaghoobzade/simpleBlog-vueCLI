<template>
  <div class="container mx-auto">
    <div class="pt-20">
      <h1 class="text-3xl font-bold pb-8">Home Page</h1>
      <p class="text-justify">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ad magni
        deleniti cumque ex ipsam minus ullam repellendus suscipit voluptate,
        veniam atque ipsa temporibus totam dicta assumenda a modi nemo
        dignissimos? Laborum repellendus accusamus quaerat totam neque nam hic
        laboriosam beatae fuga illo iste numquam reprehenderit necessitatibus
        eum, alias temporibus facilis. Lorem ipsum dolor sit amet consectetur,
        adipisicing elit. Nobis fugiat, atque iste unde ab repudiandae sapiente
        mollitia odit velit aliquam amet consequatur blanditiis repellat
        voluptate quaerat ipsam cum fugit quisquam? Deleniti quas suscipit vero
        perferendis numquam impedit itaque animi laudantium assumenda autem.
        Quos reprehenderit quibusdam optio inventore sint eligendi voluptate
        ipsa rem quo distinctio, sed laboriosam dolorum provident nobis, eveniet
        porro quis officiis, aspernatur minima aperiam cum nulla! Sint beatae
        consectetur dignissimos saepe! Enim pariatur similique, consequatur
        maiores error iure praesentium iste, rem possimus ducimus quod nisi est
        tempora unde officia. Hic dignissimos vitae harum assumenda explicabo
        accusamus perferendis facere.
      </p>
      <router-link :to="{ name: 'users' }" class="inline-block mt-4 mr-2 py-2 px-4 bg-black text-white font-medium rounded-md">Users</router-link>
      <router-link :to="{ name: 'posts' }" class="inline-block mt-4 py-2 px-4 bg-gray-100 font-medium rounded-md">Posts</router-link>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>