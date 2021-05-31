<template>
    <div class="container">
        <LargeCardDisplay
            v-for="item in largeCardInfo.slice(0, 1)" 
            :key="item.id"
            :cardsSection="item"
         />

         <SmallCardDisplay
            v-for="item in smallCardInfo.slice(0, 1)" 
            :key="item.id"
            :cardsSection="item"
         />
    </div>
</template>

<script>
    import { largeCardSections, smallCardSections } from "@/assets/data"
    export default {
        data() {
            return {
                largeCardInfo: largeCardSections,
                smallCardInfo: smallCardSections
            }
        }
    }
</script>

<style scoped>

</style>