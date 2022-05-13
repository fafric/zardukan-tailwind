<template>
   <div class="mb-4">
    <button @click="$emit('click-event')" :class="sizeClass" class="rounded font-medium border-2 border-blue-300 text-blue-500 bg-blue-200 focus:outline-none hover:bg-blue-300">{{text}}</button>
  </div>
</template>

<script>
export default {
 props: {
     size: Number,
     text: String
 },
 emits: ['click-event'],
 computed: {
     sizeClass () {
         switch (this.size) {
             case 1:
                 return "mx-2 px-2 py-1 text-xs"
                 break;
             case 2:
                 return "mx-2 px-4 py-2 text-sm"
                 break;
              case 3:
                 return "mx-2 my-2 px-8 py-4 text"
                 break;
             default: return "mx-2 my-2 px-8 py-4 text"
                 break;
         }
     }
 }
 
}
</script>

<style>

</style>