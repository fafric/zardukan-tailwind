<template>
  <div>
    <nav-bar @menu="userManue = !userManue" :mydropmenu="userManue" />
    <main>
      <div class="flex flex-col md:flex-row">
        <side-bart />
        <section class="container mx-auto pt-8">
           
                <div class="bg-gray-800 pt-6">
                      <div class="rounded-tl-3xl bg-gradient-to-r from-blue-900 to-gray-800 p-4 shadow text-2xl text-white">
                          <h1 class="font-bold pl-2">{{$route.name}}</h1>
                      </div>
                </div>
                 <div class="flex flex-wrap">
                    <div class="w-full  xl:w-1/3 p-6">
                       <Nuxt />
                    </div>
                 </div>
           
        </section>
      </div>
    </main>
  </div>
</template>

<script>
export default {
data() {
      return {
        userManue: false
      }
    },
}
</script>

<style>
 @import url("https://use.fontawesome.com/releases/v5.3.1/css/all.css");
</style>