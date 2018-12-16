<template>
  <div class="present-box" :style="boxStyle">
    <div class="present-cap" :style="capStyle"></div>
    <div class="present-body" :style="bodyStyle"></div>
    <div class="present-ribbon" :style="ribbonStyle"></div>
  </div>
</template>

<script>
export default {
  name: "Present",
  props: {
    size: {
      type: Number,
      default: 30
    },
    boxColor: {
      type: String,
      default: "#82dfe3"
    },
    ribbonColor: {
      type: String,
      default: "#69b2cb"
    }
  },
  data: function() {
    return {
      boxStyle: {
        width: this.size + 2 + "px"
      },
      capStyle: {
        height: this.size / 3 + "px",
        "background-color": this.boxColor
      },
      bodyStyle: {
        "background-color": this.boxColor,
        height: (this.size * 2) / 3 + "px"
      },
      ribbonStyle: {
        "background-color": this.ribbonColor,
        width: this.size / 6 + "px",
        left: this.size / 6 + 2 + "px"
      }
    };
  },
  created: function() {},
  mounted: function() {},
  methods: {}
};
</script>

<style scoped>
.present-box {
  position: relative;
  display: flex;
  flex-direction: column;
  width: 32px;
}
/** 阴影特效 */
/** 阴影应交给调用方解决 */
/* .present-box:after {
  background-color: #e7eff7;
  bottom: -2px;
  border-radius: 7px;
  content: "";
  display: block;
  height: 7px;
  left: 3px;
  position: absolute;
  width: calc(100% + 2px);
} */
.present-cap {
  border-radius: 4px 4px 2px 2px;
  box-shadow: 0 2px 0 0 rgba(0, 0, 0, 0.04);
  z-index: 1;
}
.present-cap:before {
  content: "";
  display: block;
  width: 100%;
  height: 100%;
  background: rgba(255, 255, 255, 0.2);
}
.present-body {
  border-bottom-left-radius: 4px;
  border-bottom-right-radius: 4px;
  margin: auto;
  width: calc(100% - 2px);
	z-index: 1;
}
.present-ribbon {
  position: absolute;
  z-index: 9999;
  height: 100%;
}
</style>
