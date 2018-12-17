<template>
  <div class="legs">
    <div class="leg-left">
      <div class="anim-part">
        <div class="line"></div>
      </div>
    </div>
    <div class="leg-right">
      <div class="anim-part">
        <div class="circle">
          <div class="circle">
            <div class="circle">
              <div class="circle">
                <div class="circle">
                  <div class="circle">
                    <div class="circle">
                      <div class="circle">
                        <div class="circle circle-last"></div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ElkLegs",
  props: {},
  data: function() {
    return {};
  },
  created: function() {},
  mounted: function() {},
  methods: {}
};
</script>

<style scoped>
.legs {
  position: relative;
}
.legs:before {
  background: -webkit-linear-gradient(right, #91655d 50%, #9c7169 50%);
  background: linear-gradient(to left, #91655d 50%, #9c7169 50%);
  bottom: 0;
  content: "";
  display: block;
  height: 10px;
  left: 7px;
  position: absolute;
  width: 30px;
  z-index: 0;
}
.leg-left:before,
.leg-left:after,
.leg-right:before,
.leg-right:after {
  content: "";
  display: block;
  position: absolute;
  z-index: 1;
}
.leg-left .anim-part {
  -webkit-animation: leg-left 0.4s ease-out infinite alternate-reverse;
  animation: leg-left 0.4s ease-out infinite alternate-reverse;
  position: relative;
  top: 1px;
  -webkit-transform: rotate(5deg) translateX(3px);
  transform: rotate(5deg) translateX(3px);
  -webkit-transform-origin: right;
  transform-origin: right;
  z-index: 2;
}
.leg-left .anim-part:before,
.leg-left .anim-part:after {
  content: "";
  display: block;
  position: absolute;
  z-index: 1;
}
.leg-left .anim-part:before {
  height: 16px;
  width: 16px;
  border: 20px solid;
  border-radius: 30px;
  border-color: transparent #835f5b transparent transparent;
  -webkit-transform: rotate(-45deg);
  transform: rotate(-45deg);
  top: -17px;
  left: 17px;
}
.leg-left .anim-part .line {
  background-color: #835f5b;
  height: 25px;
  position: absolute;
  width: 20px;
  left: 51px;
  top: 7px;
  z-index: 2;
  -webkit-transform: skew(-9deg);
  transform: skew(-9deg);
}
.leg-left .anim-part:after {
  background-color: #835f5b;
  height: 20px;
  left: 33px;
  top: -20px;
  width: 24px;
}
.leg-left:after {
  background-color: #674a4a;
  height: 13px;
  left: 48px;
  top: 32px;
  -webkit-transform: skew(-8deg);
  transform: skew(-8deg);
  width: 20px;
  z-index: 2;
}
.leg-right {
  position: relative;
  right: 10px;
}
.leg-right:before {
  height: 30px;
  width: 38px;
  border: 20px solid;
  border-radius: 40px;
  border-color: #91655d transparent transparent transparent;
  -webkit-transform: rotate(-15deg);
  transform: rotate(-15deg);
  z-index: 3;
  top: -29px;
  left: 21px;
}
.leg-right .anim-part {
  position: absolute;
  left: 64px;
  bottom: 9px;
  -webkit-transform: rotate(43deg);
  transform: rotate(43deg);
  z-index: 2;
}
.leg-right .anim-part .circle {
  -webkit-animation: leg-right 0.4s ease-out infinite alternate-reverse;
  animation: leg-right 0.4s ease-out infinite alternate-reverse;
  width: 20px;
  height: 20px;
  background-color: #91655d;
  border-radius: 20px;
  -webkit-transform: translateX(4px) rotate(4deg);
  transform: translateX(4px) rotate(4deg);
}
.leg-right .anim-part .circle-last {
  border-radius: 20px 0 0 20px;
}
.leg-right .anim-part .circle-last:before {
  content: "";
  display: block;
  border-bottom: 20px solid #674a4a;
  border-right: 2px solid transparent;
  height: 0;
  left: 15px;
  width: 11px;
  position: relative;
  z-index: 1;
}
@-webkit-keyframes leg-left {
    0% {
        -webkit-transform: rotate(0deg) translateX(0px);
        transform: rotate(0deg) translateX(0px);
    }
    50% {
        -webkit-transform: rotate(5deg) translateX(3px);
        transform: rotate(5deg) translateX(3px);
    }
}
@keyframes leg-left {
    0% {
        -webkit-transform: rotate(0deg) translateX(0px);
        transform: rotate(0deg) translateX(0px);
    }
    50% {
        -webkit-transform: rotate(5deg) translateX(3px);
        transform: rotate(5deg) translateX(3px);
    }
}
@-webkit-keyframes leg-right {
    to {
        -webkit-transform: translateX(4px) rotate(2deg);
        transform: translateX(4px) rotate(2deg);
    }
}
@keyframes leg-right {
    to {
        -webkit-transform: translateX(4px) rotate(2deg);
        transform: translateX(4px) rotate(2deg);
    }
}
</style>
