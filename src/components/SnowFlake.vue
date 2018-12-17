// TODO:
// 雪花轮廓模糊实现
// 雪花轨迹优化
// 内联keyframe实现
// 背景图实现
// canvas实现

<template> 
  <div>
    <div v-for="(snowflake, index) in snowflakes" :key="index" class="snowflake_" :style="{transform: snowflake.transform, transition: snowflake.transition}"></div>
  </div>
</template>

<script>
export default {
  name: "SnowFlake",
  props: {
    count: String
  },
  data: function() {
    return {
      snowflakes: []
    };
  },
  created: function() {
    for (let i = 0; i < Number(this.count); i++) {
      const transformX = Math.random() * 450;
      const transitionTime = 8 + Math.random() * 4;
      const scale = Math.random() * 3;
      const  beginTransform = `translate(${transformX}px, ${Math.random()*(-100)}px)`;
      let snowflake = {
        transition: `transform ${transitionTime}s`,
        transform: beginTransform,
        beginTransform: beginTransform,
        endTransform: `translate(${transformX + Math.random()*100 - 50}px, ${300 + Math.random()*200}px) scale(${scale})`,
        transitionTime: transitionTime,
      };
      this.snowflakes.push(snowflake);
    }
  },
  mounted: function() {
    this.snowflakes.forEach(item => {
      const transitionCatch = item.transition;
      const that = item;
      item.wave = () => {
        that.transition = transitionCatch;
        that.transform = that.endTransform;
        setTimeout(function() {
          that.transition = "";
          that.transform = that.beginTransform;
          setTimeout(that.wave, 100);
        }, that.transitionTime * 1000);
      };
      item.wave();
    });
  },
  methods: {
  }
};
</script>

<style scoped>
.snowflake_ {
  /* background-color: #e4e4e4; */
  background-color: #f0f0f0;
  border-radius: 100%;
  height: 3px;
  position: absolute;
  top: 0;
  width: 3px;
  z-index: 3;
  animation: snow-100 14s infinite;
}
</style>
