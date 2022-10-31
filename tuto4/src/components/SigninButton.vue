<template>
  <div>
    <p>Test a message : {{message}}</p>
    <button class="user" @click="cli()">Sign in</button>
  </div>
</template>

<script>
import {signInAndGetUser} from '../lib/microsoftGraph.js'

export default {
  name: 'SigninButton',
  props: ["message"],
  data(){
    return{
    }
  },
  methods: {
    cli(){
      this.$emit("customEventName", "blablabla");
      signInAndGetUser();
    },
  },
}
</script>

<style scoped>
button{
    height: 50px;
    width: 80px;
    background-color: #42b983;
    color: black;
    border-radius: 10%;
}
</style>
