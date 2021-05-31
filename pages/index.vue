<template>
  <div>
    <!-- <Nav /> -->
    <div class="container">
      
      <Hero /> <!--Nuxt on default does auto import, no need to specify component import-->
      <!--[:cardsSection] is the name of the props that's being passed down to the component-->
      <LargeCardDisplay v-for="item in largeCardInfo" :key="item.id"  :cardsSection="item" />
      <!--In Vue...Instead of writing JSX to map through each item and drop it in as prop, you map it in line--->
      <SmallCardDisplay v-for="item in smallCardInfo" :key="item.id" :cardsSection="item" />
    </div>
  </div>
</template>

<script>
import Hero from '~/components/Hero.vue'
import LargeCardDisplay from '~/components/LargeCardDisplay.vue'
import SmallCardDisplay from '~/components/SmallCardDisplay.vue'
import { largeCardSections, smallCardSections } from "@/assets/data.js" // @ means root directory
import Nav from '~/components/Nav.vue'


export default {
  data() {
    return {
      // states 
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  },
  components: { 
    Hero,
    LargeCardDisplay,
    SmallCardDisplay,
    Nav
    },
  }
</script>

<style>

</style>
