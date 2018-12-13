<template>
    <div>
        <div class="row">
            <div class="col-sm-8" v-if="!isSubmitted">
                <h2>Add information about your event</h2>
                <form>
                <div class="form-group">
                    <label>Event name</label>
                    <input type='text' class='form-control' v-model.lazy="eventName">
                </div>  
                <div class="form-group">
                    <label>How many guests will be on the event?</label>
                    <input class='form-control' v-model.lazy="guestsNumber">
                </div>
                <button type='submit' @click.prevent="infoEventSubmit" class="btn btn-light">Submit</button>    
                </form>
            </div>
        </div>
        <div class="row">
            <div class='col-sm-8' v-if="isSubmitted">
                <h3>Information about your event</h3>
                <p>Event name: {{eventName}}</p>
                <p>Number of guests: {{guestsNumber}}</p>
            </div>
        </div>
    </div>    
</template>

<script>
    export default {
        data () {
            return {
                eventName : '',
                guestsNumber: 0,
                isSubmitted: false
            }
        },
        methods: {
            infoEventSubmit() {
                this.isSubmitted = true;
            }
        }
    }

</script>

<style>
</style>