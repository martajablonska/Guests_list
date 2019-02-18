<template>
    <div>
        <div class="row">
            <div class="col-sm-4">
                <h3>Add new guest to your event</h3>
                <form>
                    <div class="form-group">
                        <label>Guest name</label>
                        <input type='text' class='form-control' v-model.lazy="guest">
                    </div> 
                    <button type='submit' class='btn btn-light' @click.prevent='addGuest'>Add guest</button>
                </form>    
            </div>
        </div>
    </div>    
</template>

<script>
    export default {
        data() {
            return {
                guest: ''
            };
        },
        methods: {
            addGuest() {
                this.$emit('guestAdded', this.guest);
                this.guest = '';
            }
        }
    }

</script>

<style>
</style>
