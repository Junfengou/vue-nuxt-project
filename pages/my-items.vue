<template>
    <div>
        <MyItem 
            v-for="rental in myRentals"
            :key="rental.id"
            :item="rental"
        />
    </div>
</template>

<script>
    import { mapState  } from "vuex" 
    export default {
        // defining this component to use [no-nav] layout so it doesn't use nav while other component stay the same
        layout: 'no-nav' ,
        computed: {
            ...mapState([
                'myRentals'
            ])
        }
    }
</script>

<style scoped>
    .container {
        padding: 5rem 0
    }
</style>