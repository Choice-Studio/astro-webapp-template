<template>
  <div class="hidden lg:flex">

    <header class="w-full h-16 bg-primary flex items-center px-8">

      <div class="flex items-center w-1/3">
        <h6 class="text-white ml-2 font-body">ASTRO TEMPLATE</h6>
      </div>

      <div class="w-2/3 flex items-center justify-end text-white">
        <a :key="page.pageName" v-for="page in pages" :href="page.pageHREF" class="uppercase font-size-16 mx-8" :class="[pageName == page.pageName ? 'underline' : '']">{{ page.pageName }}</a>
      </div>

    </header>

  </div>
</template>


<script lang="ts">
import pageData from '../../data/pageData.json';

export default {
  name: 'DesktopHeader',
  props: {
    pageName: String
  },
  data () {
    return {
      pages: pageData,
    };
  },
  // components: {
    
	// },
  // data () {
  //   return {
      
  //   }
  // },
  // methods: {

  // },
  // created () {

  // }
}

</script>


<style scoped lang="scss">
  @use '../../sass/abstracts' as *;
  @use '../../sass/themes' as *;



</style>