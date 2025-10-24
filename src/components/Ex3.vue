<script>
    export default { 

       // add code here
       data(){
        return{
            UN : {name : "Username login", value:"0"},
            Email : {name : "Email login", value:"1"},
            Selected_name : ""

        }
       }

    }
</script>

<template>
    <h1>Please select your login option</h1>
    <!-- Add/modify code in the following to have a dropdown list 
        which lets the user to select either to login with username or email -->
    <select v-model="Selected_name">
        <option :value="UN.name" selected >{{UN.name}}</option>
        <option :value = "Email.name">{{ Email.name }}</option>
    </select>
    
    <div v-if="Selected_name===UN.name">

        <label>Username</label>
        <input placeholder="Enter your username">
        
    </div>

    <div v-else>

        <label>Email</label>
        <input placeholder="Enter your email">
        
    </div>

    <!-- can add condition if wanted -->
    <!-- <div v-else="Selected_val===Email.value">

        <label>Email</label>
        <input placeholder="Enter your email">
        
    </div> -->
    
</template>

