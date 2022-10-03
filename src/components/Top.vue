<template>
    <div class="topStyle">
        <div style="margin-left: 25%">
            <b-button @click="primaryClicked" style="margin: 1%; width: 15%" variant="primary">Primary</b-button>
            <b-button style="margin: 1%; width: 15%" variant="secondary">Secondary</b-button>
            <b-button style="margin: 1%; width: 15%" variant="success">Success</b-button>
            <b-button style="margin: 1%; width: 15%" variant="danger">Danger</b-button>
        </div>
        <b-input-group prepend="New user" style="width:50%; margin-left:25.5%; margin-top: 1%">
            <b-form-input placeholder="Name here" v-model="username"></b-form-input>
            <b-form-input placeholder="Age here" v-model="age"></b-form-input>
            <b-input-group-append>
            <b-button @click="InputUsername" variant="info">Enter</b-button>
            </b-input-group-append>
        </b-input-group>
    </div>
</template>
    
<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    setup () {
        let username = ref(undefined);
        let age = ref(undefined);
        function primaryClicked(){
            console.log("primary button clicked")
        }
        function InputUsername(){
            console.log('name: ', username.value, ' age: ', age.value);
        }

        return {
            primaryClicked,
            InputUsername,
            username,
            age
        }
    }
})
</script>

<style scoped>
    .topStyle {
        border-style: solid;
        border-color: red;
        height: 20%
    }
</style>