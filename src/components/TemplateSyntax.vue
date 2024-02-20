<template>
    <div class="header">
        <div class="bugheader">
            <h1>{{ message }}</h1>
            <div class="inputs">
                <div> <p>Area of a bank: {{ selected }}</p></div>
                <select v-model="selected">
                    <option disabled value=""> please select one area</option>
                    <option>Bangalore</option>
                    <option>chennai</option>
                    <option>Hyderabad</option>
                    <option>Mumbai</option>
                </select>
                <br>
    
                <input type="text" placeholder="Aadhar number" v-model="Anumber"/><br>
                <input type="text" placeholder="pan number" v-model="Pnumber"/><br>
                <input type="text" placeholder="Phone number" pattern="[0-9]" v-model="number"/>
                <br>           
                <span>Enter the message that you are facing</span>
                <p style="white-space: pre-line;">{{ }}</p>
                <textarea   v-model="message2" placeholder="ellaborate here"></textarea>
            </div>
        </div>
    </div>
    <br>
    <hr>
    <div class="box">
    <div class="myworld">
    <ul class="display1">
        <li>{{ selected }}</li>
        <li> {{ Anumber }}</li>
        <li>{{ Pnumber }}</li>
        <li>{{  number}}</li>
        <li>{{ message2 }}</li>
    </ul>
</div>
</div>
    
    


    
</template>


<script setup>
  import { ref } from 'vue';
     const message='Banking Bug from service count';
     const selected=ref('');
     const Anumber=ref('');

     const Pnumber=ref('');
     const number=ref('');
     const message2=ref('');

     
    



</script>
<style>
.header{
    width: 50%;
    margin: 0 auto;
}
.bugheader{
    background-color: rgb(229, 240, 240);
    align-items: center;
   
    width:100%;
    height: 400px;
    padding:50px;
    justify-content: center;
}
input {
    width:100%;
    height: 20px;
    margin: 10px;
}
textarea{
    height: 100%;
    width: 100%;
}
.display1{
    align-items: center;
    list-style-type: none;
    
}

.myworld{
    align-items: center;
    background-color: azure;

}
li{
    text-decoration: none;
    font-size: medium;
    text-align: center;

}
.box{
    align-items: center;
    display: inline;
    
}



</style>