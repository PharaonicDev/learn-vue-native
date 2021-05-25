<template>
  <view class="container" >
    <animated:view
      class="growth-animated-view"
      :style="{
        height: growth,
        width: growth ,
        borderRadius:growth,
      }"
    />
  </view>
</template>

<style>
.growth-animated-view {
  background-color: "rgb(0, 138, 231)";
  align-self: center;
}

.container {
  justify-content: center;
  flex: 1;
}
</style>

<script>
import { Animated, Easing } from "react-native";

export default {
  data: function() {
    return {
      growth: 0
    };
  },
  created: function() {
    this.growth = new Animated.Value(0);
  },
  mounted: function() {
    this.animateGrowth();
  },
  methods: {
    animateGrowth: function() {

      this.growth.setValue(0);

      Animated.timing(this.growth, {
        toValue: 200,
        duration: 1000,
        easing: Easing.linear
      }).start(() => {
        // this.animateGrowth();
      });
    }
  }
};
</script>