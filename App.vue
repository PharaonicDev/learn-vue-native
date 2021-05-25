<template>
  <view class="container">
  <text class="text-login">Login</text>
 
    <text-input
      class="text-input-container"
      placeholder="user name"
      v-model="textContent"
    />
    <text-input 
     class="text-input-container"
     placeholder="password"
     />
    <text class="text-container">{{textContent}}</text>
</view>
  </template>

 <script>
export default {
  data: function() {
    return {
      textContent: ""
    };
  }
};
</script>
 <style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-container {
  color: blue;
  padding: 2;
  font-size: 22;
}
.text-login {
  font-size:30;
  color:gray;
 justify-content: center;
}
.text-input-container {
  width: 300;
  height: 60;
  font-size: 22;
  border-color: 
}
</style>
