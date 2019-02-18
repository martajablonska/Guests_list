<template>
    <div class='col-sm-4'>
        <li>
            <div class="guest">
                <slot></slot>
            </div>
        </li>    
    </div>
</template>

<script>
</script>

<style>
    .guest {
        cursor:pointer;
        height: 50px;
    }
    .guest:hover {
        background-color: #ffa9a9;
    }
</style>