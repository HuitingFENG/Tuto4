<template>
  <ul>
    <li><a href="#home">Home</a></li>
    <li><a href="#news">News</a></li>
    <li><a href="#contact">Contact</a></li>
    <li style="float:right"><SigninButton message="ping" @customEventName="handleCustomEvent" /></li>
  </ul>
</template>

<script>
import SigninButton from './SigninButton.vue'

export default {
  name: 'HomePage',
  components:{
    SigninButton,
  },
  methods:{
      handleCustomeEvent(){
          console.log('this is a test');
      }
  }
};
</script>

<style scoped>
body {
  font-size: 50px;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
  position: -webkit-sticky;
  position: sticky;
  top: 0;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #111;
}

</style>
