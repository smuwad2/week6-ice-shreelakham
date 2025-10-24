<script>
    export default { 
        data() {
            return {
                width: '200',
                height: '200',
                myImg: '/assets/me.png'
            }
        },
    }
</script>

<template>

    <!-- add code here -->
     <div id="demo1">
        <img v-bind:src ="myImg"></img>
    </div>
   
</template>
