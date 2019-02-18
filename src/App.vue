<template>
    <div class="container">
        <app-event-form></app-event-form>
        <!--progress bar with a number of guests-->
        <app-guest-form @guestAdded="addGuestToList"></app-guest-form>
        <app-guest-list :guests="guests"></app-guest-list>
        <!--guests list-->
    </div>
</template>

<script>
    import EventForm from './components/EventForm.vue';
    import GuestForm from './components/GuestForm.vue';
    import GuestList from './components/GuestList.vue';
    
    export default {
        data () {
            return {
                guests : []
            };
        },
        components : {
            'app-event-form' : EventForm,
            'app-guest-form' : GuestForm,
            'app-guest-list' : GuestList
        },
        methods: {
            addGuestToList(guest) {
                this.guests.push(guest);
            }
        }
    }
</script>

<style>
</style>
