<template>
    <div class="container">
        <app-event-form></app-event-form>
        <!--progress bar with a number of guests-->
        <app-guest-form @guestAdded="addGuestToList"></app-guest-form>
        <!--guests list-->
    </div>
</template>

<script>
    import EventForm from './components/EventForm.vue';
    import GuestForm from './components/GuestForm.vue';
    
    export default {
        data () {
            return {
                guests : []
            };
        },
        components : {
            'app-event-form' : EventForm,
            'app-guest-form' : GuestForm
        },
        methods: {
            addGuestToList() {
                this.guests.push(guest);
            }
        }
    }
</script>

<style>
</style>
