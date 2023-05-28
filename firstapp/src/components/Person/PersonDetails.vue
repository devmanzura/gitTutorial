<template>
   <div class="person-details">
      <div>
         <img :src="getImg" alt="Avatar">
      </div>

   </div>
</template>
<script >
export default {
   name:"PersonDetails"
   ,props:{
      person:{
         type:Object
         
      }
   }
}
</script>
<style lang="">
   
</style>