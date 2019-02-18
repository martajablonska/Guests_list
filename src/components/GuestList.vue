<template>
    <div class='row'>
        <app-guest v-for='(guest, index) in guests'> {{ guest }}</app-guest> 
                                            
    </div>
</template>

<script>
    import Guest from './Guest.vue';
    export default {
        props: ['guests'],
        components: {
            'appGuest':Guest
        }
    }
</script>

<style>
</style>