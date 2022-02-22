<template>
   <table class="w-full text-left">
      <thead>
         <tr>
            <th class="block text-lg font-semibold bg-blue-500 text-white p-4 border border-blue-500 rounded-t">
               <router-link :to="{ name: 'userId', params: { id: user.id } }">{{ user.name }} </router-link>
            </th>
         </tr>
      </thead>
      <tbody>
         <tr>
            <td class="block font-medium py-3 px-4 border-b border-l border-r border-[#E8E8E8]">Username: {{ user.username }}</td>
         </tr>
         <tr>
            <td class="block font-medium py-3 px-4 border-b border-l border-r border-[#E8E8E8]">Email: {{ user.email }}</td>
         </tr>
         <tr>
            <td class="block font-medium py-3 px-4 border-b border-l border-r border-[#E8E8E8] rounded-b">Phone: {{ user.phone }}</td>
         </tr>
      </tbody>
   </table>
</template>

<script>
export default {
   props:{
      user: Object,
   }

}
</script>

<style>

</style>