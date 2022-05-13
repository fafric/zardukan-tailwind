<template>
  <div>
    <h1 class="pt-2" >hello this is index page</h1>
    <t-button @click="test()" class="ml-4"  variant="success">Example button</t-button>
    <t-tag tag-name="span" variant="avatar">new</t-tag>
    <my-button :size="3" text="Click Me" @click-event="test"> </my-button>
    <t-datepicker v-model="dateselect" />
    <t-datepicker
      v-model="dateselect1"
    >
      <template
        slot="day"
        slot-scope="{ day, dayFormatted }"
      >
        <span v-if="birthdays.includes(day)">
          🎂
        </span>
        <span v-else-if="day.getDay() === 6">
          🌮
        </span>
        <span v-else>
          {{ dayFormatted }}
        </span>
      </template>
    </t-datepicker>
  </div>
  
</template>

<script>
import myButton from '~/components/myButton.vue'

export default {
  components: { myButton },
  layout:'dashboard',
  name: 'IndexPage',
  data() {
      return {
       dateselect: null ,
       dateselect1: null ,
       birthdays: [ 4, 6]
      }
    },
  methods: {
   test () {
     alert('what is this?')
     console.log('hello world!');
   }
  }
}
// https://github.com/tailwindtoolbox/Admin-Template/blob/master/index.html
</script>
<style scoped>

</style>
