<template>
    <div class="container">
        <app-event-form></app-event-form>
        <!--progress bar with a number of guests-->
        <!--form to add guest-->
        <!--guests list-->
    </div>
</template>

<script>
    import EventForm from './components/EventForm.vue';
    
    export default {
        components : {
            'app-event-form' : EventForm
        }
    }
</script>

<style>
</style>
