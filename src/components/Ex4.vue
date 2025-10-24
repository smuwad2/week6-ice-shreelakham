<script>
    export default { 
        data() {
            return {
                // Add code 
                redbtn : "btn btn-danger",
                bluebtn : "btn btn-primary",
                counter : 0,
                id : "demo1",
                currentClass : "btn btn-primary",
                Blueactive : true,
                Redactive : false

        }
    },
        methods : { 
   			// Add code here
            addClass(){
            this.counter +=1;
            if(this.counter%2 ==1){
                this.currentClass = this.redbtn;
                this.Redactive = true;
                this.Blueactive = false
            }
            else{
                this.currentClass = this.bluebtn;
                this.Redactive = false;
                this.Blueactive = true
            }
            



            }
            

		}
    
}
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="id" class="m-2" v-bind:class="{'blueBox' : Blueactive, 'redBox': Redactive}">
            div ID : {{id}} 
        </div>
        
        <button v-bind:class="[currentClass]"
        v-on:click="addClass"
        
        type="button">Change Color</button>
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
