<template>
  <div>
      <h1>SigninButton</h1>
      <button @click="signInAndGetUser()">Sign in</button>
  </div>
</template>

<script>
import {signInAndGetUser} from '../lib/microsoftGraph.js'

export default {
  name: 'SigninButton',
  props: {
    msg: String
  },
  data(){
    signInAndGetUser()
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
