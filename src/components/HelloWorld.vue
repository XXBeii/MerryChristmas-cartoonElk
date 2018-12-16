<template>
<div class="container">
    <div class="artboard">
        <div class="deer">
            <div class="rocking">
                <div class="head">
                    <div class="horns">
                        <div class="horn horn-left">
                            <div class="line line-one"></div>
                            <div class="line"></div>
                            <div class="line line-three"></div>
                        </div>
                        <div class="horn horn-right">
                            <div class="line line-one"></div>
                            <div class="line"></div>
                            <div class="line line-three"></div>
                        </div>
                    </div>
                    <div class="ears">
                        <div class="ear ear-left"></div>
                        <div class="ear ear-right"></div>
                    </div>
                    <div class="eyes">
                        <div class="eye eye-left"></div>
                        <div class="eye eye-right"></div>
                    </div>
                    <div class="nose"></div>
                </div>
                <div class="body">
                    <div class="shadow"></div>
                    <div class="hooves">
                        <!-- <div class="hoof-one">
                            <div class="line"></div>
                            <div class="anim-part">
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
                        <div class="hoof-two">
                            <div class="line-one"></div>
                            <div class="line-two"></div>
                        </div> -->
                    </div>
                </div>
                <!-- <div class="tail">
                    <div class="circle">
                        <div class="circle">
                            <div class="circle">
                                <div class="circle">
                                    <div class="circle"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div> -->
            </div>
            <!-- <div class="legs">
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
            </div> -->
        </div>
        <div class="presents">
            <!-- 红色 -->
            <Present class="present present-one" :size="45" boxColor="#fb5d5d" ribbonColor="transparent"/>
            <Present class="present"/>
            <Present class="present present-two-right"/>
            <!-- 黄色 -->
            <Present class="present present-three" :size="25" boxColor="#ffb63c" ribbonColor="#fb5353" />
        </div>
        <div class="snow"></div>
        <SnowFlake count="50" />
    </div>
</div>
</template>

<script>
import SnowFlake from './SnowFlake.vue'
import Present from './Present.vue'

export default {
  name: 'HelloWorld',
  components: {
    SnowFlake,
    Present
  },
  props: {
    msg: String
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url(https://fonts.googleapis.com/css?family=Open+Sans:400,600);
.container {
    background-color: white;
    border-radius: 4px;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
    height: 300px;
    margin: 40px auto 50px auto;
    position: relative;
    width: 450px;
}
.artboard {
    height: 100%;
    overflow: hidden;
    position: relative;
    width: 100%;
}
.deer {
    width: 50px;
    margin: 0 auto;
    position: relative;
}
.rocking {
    -webkit-animation: rocking 0.4s ease-in-out infinite alternate-reverse;
    animation: rocking 0.4s ease-in-out infinite alternate-reverse;
    -webkit-transform-origin: bottom left;
    transform-origin: bottom left;
    position: relative;
    z-index: 1;
}
.head {
    position: relative;
    width: 50px;
}
.horns {
    -webkit-animation: rocking 0.4s cubic-bezier(0.4, 0, 0.2, 1) infinite alternate-reverse;
    animation: rocking 0.4s cubic-bezier(0.4, 0, 0.2, 1) infinite alternate-reverse;
    height: 55px;
    position: relative;
    top: 21px;
    width: 50px;
}
.horn {
    position: relative;
}
.horn:before {
    background-color: #91655d;
    border-radius: 7px 7px 0 0;
    content: "";
    display: block;
    height: 55px;
    position: absolute;
    width: 7px;
    z-index: 1;
}
.horn .line {
    background-color: #91655d;
    border-radius: 7px 0 0 7px;
    height: 7px;
    width: 20px;
    margin-bottom: 15px;
    position: relative;
    top: 10px;
}
.horn .line-one {
    width: 15px;
}
.horn .line-three {
    top: -22px;
    width: 17px;
}
.horn-left {
    top: -7px;
    -webkit-transform: rotate(-25deg);
    transform: rotate(-25deg);
}
.horn-left:before {
    box-shadow: inset 2px 0 0 0 #9c7169;
}
.horn-left .line {
    box-shadow: inset 0 2px 0 0 #9c7169;
    right: 15px;
    -webkit-transform: rotate(30deg);
    transform: rotate(30deg);
}
.horn-left .line-one {
    right: 10px;
}
.horn-left .line-three {
    box-shadow: inset 0 -2px 0 0 #9c7169;
    right: -3px;
    -webkit-transform: rotate(160deg);
    transform: rotate(160deg);
}
.horn-right {
    bottom: 55px;
    left: 40px;
    -webkit-transform: rotate(25deg);
    transform: rotate(25deg);
}
.horn-right:before {
    box-shadow: inset -2px 0 0 0 #835f5a;
}
.horn-right .line {
    box-shadow: inset 0 2px 0 0 #835f5a;
    right: -2px;
    -webkit-transform: rotate(150deg);
    transform: rotate(150deg);
}
.horn-right .line-three {
    right: 13px;
    -webkit-transform: rotate(20deg);
    transform: rotate(20deg);
}
.ears {
    position: absolute;
    top: 70px;
}
.ear {
    background-color: #91655d;
    border-radius: 100% 50% 50% 50%;
    height: 18px;
    position: relative;
    right: 20px;
    top: 10px;
    -webkit-transform: rotate(30deg);
    transform: rotate(30deg);
    -webkit-transform-origin: 100%;
    transform-origin: 100%;
    width: 30px;
}
.ear:before {
    background-color: #e7beb2;
    border-radius: 100% 50% 50% 50%;
    height: 9px;
    content: "";
    display: block;
    left: 5px;
    position: relative;
    top: 5px;
    width: 15px;
}
.ear-left {
    -webkit-animation: ear-left 2s cubic-bezier(0.6, -0.28, 0.74, 0.05) infinite alternate-reverse;
    animation: ear-left 2s cubic-bezier(0.6, -0.28, 0.74, 0.05) infinite alternate-reverse;
    -webkit-transform: rotate(30deg);
    transform: rotate(30deg);
}
.ear-right {
    -webkit-animation: ear-right 2s cubic-bezier(0.6, -0.28, 0.74, 0.05) 2s infinite alternate-reverse;
    animation: ear-right 2s cubic-bezier(0.6, -0.28, 0.74, 0.05) 2s infinite alternate-reverse;
    left: 10px;
    right: 0;
    top: -8px;
    -webkit-transform: rotate(160deg);
    transform: rotate(160deg);
}
.eyes {
    position: absolute;
    top: 90px;
    right: -5px;
    width: 32px;
    z-index: 2;
}
.eyes .eye {
    background: -webkit-linear-gradient(90deg, white 50%, #aa8275 50%);
    background: linear-gradient(0deg, white 50%, #aa8275 50%);
    border-radius: 15px;
    height: 15px;
    width: 15px;
}
.eyes .eye:before {
    -webkit-animation: eaves 3s infinite alternate-reverse;
    animation: eaves 3s infinite alternate-reverse;
    background-color: #aa8275;
    border-radius: 9px 9px 0 0;
    height: 9px;
    content: "";
    display: block;
    position: relative;
    width: 15px;
    top: -1px;
    z-index: 1;
}
.eyes .eye:after {
    -webkit-animation: eyes 3s infinite alternate-reverse;
    animation: eyes 3s infinite alternate-reverse;
    background-color: #495169;
    border-radius: 5px;
    height: 5px;
    content: "";
    display: block;
    left: 5px;
    position: relative;
    top: -3px;
    -webkit-transform: translate(3px, 2px);
    transform: translate(3px, 2px);
    width: 5px;
}
.eyes .eye-left {
    float: left;
}
.eyes .eye-right {
    float: right;
}
.nose {
    background-color: #91655d;
    border-radius: 0 7px 15px;
    top: 47px;
    height: 18px;
    left: 40px;
    position: relative;
    width: 20px;
    z-index: 2;
}
.nose:before {
    background-color: #fb5d5d;
    border-radius: 15px;
    content: "";
    display: block;
    height: 14px;
    position: absolute;
    right: -0.5px;
    top: -0.5px;
    width: 16px;
}
.nose:after {
    background-color: white;
    border-radius: 5px;
    content: "";
    display: block;
    height: 2px;
    position: absolute;
    right: 4px;
    top: 2px;
    width: 5px;
}
.body {
    background-color: #91655d;
    border-radius: 50px 50px 0;
    box-shadow: inset 7px 0 0 0 #9c7169;
    height: 140px;
    position: relative;
    width: 50px;
    z-index: 1;
}
.body:before {
    background-color: #e7beb2;
    border-radius: 20px 0 0 20px;
    bottom: 20px;
    box-shadow: inset -7px 0 0 0 #c39e9a;
    content: "";
    display: block;
    height: 65px;
    position: absolute;
    right: 0;
    width: 20px;
}
.hooves {
    position: relative;
    bottom: 40px;
    right: 34px;
}
.hoof-one {
    -webkit-animation: jump 0.3s ease-in-out infinite alternate-reverse;
    animation: jump 0.3s ease-in-out infinite alternate-reverse;
    left: 10px;
    position: relative;
    top: 70px;
    -webkit-transform: rotate(25deg);
    transform: rotate(25deg);
    -webkit-transform-origin: 100% 50%;
    transform-origin: 100% 50%;
}
.hoof-one .line {
    height: 30px;
    border: 20px solid;
    border-radius: 40px;
    border-color: transparent transparent #91655d transparent;
    left: 25px;
    width: 30px;
    position: relative;
    top: 5px;
    -webkit-transform: rotate(-30deg);
    transform: rotate(-30deg);
}
.hoof-one .anim-part {
    position: relative;
    bottom: 23px;
    left: 81px;
    -webkit-transform: rotate(-75deg);
    transform: rotate(-75deg);
    -webkit-transform-origin: left;
    transform-origin: left;
}
.hoof-one .circle {
    -webkit-animation: hoof-one 0.3s ease-in-out infinite alternate-reverse;
    animation: hoof-one 0.3s ease-in-out infinite alternate-reverse;
    background-color: #91655d;
    height: 20px;
    width: 20px;
    border-radius: 30px;
    -webkit-transform: translateX(3px) rotate(0deg);
    transform: translateX(3px) rotate(0deg);
}
.hoof-one .circle-last {
    border-radius: 20px 0 0 20px;
    -webkit-transform: translateX(2px) rotate(0deg);
    transform: translateX(2px) rotate(0deg);
}
.hoof-one .circle-last:before {
    content: "";
    display: block;
    border-top: 20px solid #674a4a;
    border-left: 7px solid transparent;
    height: 0;
    left: 10px;
    width: 7px;
    position: relative;
    z-index: 1;
}
.hoof-one .circle-last:after {
    background-color: #ffb63c;
    border-radius: 10px;
    bottom: 30px;
    content: "";
    display: block;
    height: 40px;
    left: 19px;
    position: relative;
    width: 9px;
}
.hoof-two {
    -webkit-animation: jump-two 0.3s ease-in-out infinite alternate-reverse;
    animation: jump-two 0.3s ease-in-out infinite alternate-reverse;
    left: 55px;
    position: relative;
    top: 10px;
    z-index: -1;
}
.hoof-two .line-one,
.hoof-two .line-two {
    height: 10px;
    border: 20px solid;
    border-radius: 40px;
    border-color: transparent transparent #91655d transparent;
    width: 10px;
    position: absolute;
}
.hoof-two .line-one {
    -webkit-transform: rotate(-45deg);
    transform: rotate(-45deg);
}
.hoof-two .line-two {
    left: 30px;
    -webkit-transform: rotate(135deg);
    transform: rotate(135deg);
}
.tail {
    background-color: #9c7169;
    bottom: 0;
    left: 4px;
    position: absolute;
    width: 20px;
    z-index: 0;
}
.tail .circle {
    -webkit-animation: tail 2s cubic-bezier(0, 0.02, 0.9, 2) infinite;
    animation: tail 2s cubic-bezier(0, 0.02, 0.9, 2) infinite;
    background-color: #9c7169;
    border-radius: 11px;
    height: 12px;
    position: relative;
    right: 2px;
    -webkit-transform: rotate(-5deg);
    transform: rotate(-5deg);
    width: 12px;
}
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
.presents {
    top: 3px;
    height: 45px;
    margin: 0 auto;
    position: relative;
    width: 110px;
}
.presents:after {
    -webkit-animation: shadow 0.4s ease-out infinite alternate-reverse;
    animation: shadow 0.4s ease-out infinite alternate-reverse;
    background-color: #e7eff7;
    bottom: 0;
    border-radius: 7px;
    content: "";
    display: block;
    height: 7px;
    left: -22px;
    position: absolute;
    width: 170px;
}
.present {
    bottom: 3px;
    position: absolute;
    z-index: 1;
}
.present-one {
    right: 32px;
    z-index: 2;
}
.present-two-right {
    right: 5px;
}
.present-three {
    left: 25px;
    z-index: 2;
}
.snowflake:nth-child(100) {
    -webkit-animation: snow-100 14s infinite;
    animation: snow-100 14s infinite;
}
@-webkit-keyframes snow-100 {
    from {
        -webkit-transform: translate(334px, -77px);
        transform: translate(334px, -77px);
    }
    to {
        -webkit-transform: translate(334px, 556px);
        transform: translate(334px, 556px);
    }
}
@keyframes snow-100 {
    from {
        -webkit-transform: translate(334px, -77px);
        transform: translate(334px, -77px);
    }
    to {
        -webkit-transform: translate(334px, 556px);
        transform: translate(334px, 556px);
    }
}
@-webkit-keyframes tail {
    10% {
        -webkit-transform: rotate(2deg);
        transform: rotate(2deg);
    }
    20% {
        -webkit-transform: rotate(-5deg);
        transform: rotate(-5deg);
    }
}
@keyframes tail {
    10% {
        -webkit-transform: rotate(2deg);
        transform: rotate(2deg);
    }
    20% {
        -webkit-transform: rotate(-5deg);
        transform: rotate(-5deg);
    }
}
@-webkit-keyframes shadow {
    to {
        width: 185px;
    }
}
@keyframes shadow {
    to {
        width: 185px;
    }
}
@-webkit-keyframes eyes {
    50% {
        -webkit-transform: translate(3px, 2px);
        transform: translate(3px, 2px);
    }
    60% {
        -webkit-transform: translate(0, 0);
        transform: translate(0, 0);
    }
    100% {
        -webkit-transform: translate(0, 0);
        transform: translate(0, 0);
    }
}
@keyframes eyes {
    50% {
        -webkit-transform: translate(3px, 2px);
        transform: translate(3px, 2px);
    }
    60% {
        -webkit-transform: translate(0, 0);
        transform: translate(0, 0);
    }
    100% {
        -webkit-transform: translate(0, 0);
        transform: translate(0, 0);
    }
}
@-webkit-keyframes eaves {
    50% {
        -webkit-transform: translateY(0);
        transform: translateY(0);
    }
    60% {
        -webkit-transform: translateY(-1px);
        transform: translateY(-1px);
    }
    100% {
        -webkit-transform: translateY(-1px);
        transform: translateY(-1px);
    }
}
@keyframes eaves {
    50% {
        -webkit-transform: translateY(0);
        transform: translateY(0);
    }
    60% {
        -webkit-transform: translateY(-1px);
        transform: translateY(-1px);
    }
    100% {
        -webkit-transform: translateY(-1px);
        transform: translateY(-1px);
    }
}
@-webkit-keyframes hoof-one {
    to {
        -webkit-transform: translateX(2px) rotate(5deg);
        transform: translateX(2px) rotate(5deg);
    }
}
@keyframes hoof-one {
    to {
        -webkit-transform: translateX(2px) rotate(5deg);
        transform: translateX(2px) rotate(5deg);
    }
}
@-webkit-keyframes jump {
    to {
        -webkit-transform: translateY(-2px) rotate(25deg);
        transform: translateY(-2px) rotate(25deg);
    }
}
@keyframes jump {
    to {
        -webkit-transform: translateY(-2px) rotate(25deg);
        transform: translateY(-2px) rotate(25deg);
    }
}
@-webkit-keyframes jump-two {
    to {
        -webkit-transform: translateY(2px);
        transform: translateY(2px);
    }
}
@keyframes jump-two {
    to {
        -webkit-transform: translateY(2px);
        transform: translateY(2px);
    }
}
@-webkit-keyframes rocking {
    to {
        -webkit-transform: rotate(-1deg);
        transform: rotate(-1deg);
    }
}
@keyframes rocking {
    to {
        -webkit-transform: rotate(-1deg);
        transform: rotate(-1deg);
    }
}
@-webkit-keyframes ear-left {
    85% {
        -webkit-transform: rotate(30deg);
        transform: rotate(30deg);
    }
    100% {
        -webkit-transform: rotate(-10deg);
        transform: rotate(-10deg);
    }
}
@keyframes ear-left {
    85% {
        -webkit-transform: rotate(30deg);
        transform: rotate(30deg);
    }
    100% {
        -webkit-transform: rotate(-10deg);
        transform: rotate(-10deg);
    }
}
@-webkit-keyframes ear-right {
    85% {
        -webkit-transform: rotate(160deg);
        transform: rotate(160deg);
    }
    100% {
        -webkit-transform: rotate(170deg);
        transform: rotate(170deg);
    }
}
@keyframes ear-right {
    85% {
        -webkit-transform: rotate(160deg);
        transform: rotate(160deg);
    }
    100% {
        -webkit-transform: rotate(170deg);
        transform: rotate(170deg);
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
a {
    font-weight: 600;
    color: #2196f3;
}
a:hover {
    color: #e66;
}
.title {
    color: #999;
    text-align: center;
}
.title h1 {
    font-size: 1.5em;
    margin: 100px 0 10px 0;
}
.title a {
    vertical-align: middle;
}
.title a:hover img {
    -webkit-animation: link 0.5s;
    animation: link 0.5s;
}
.title a img {
    width: 18px;
}
html,
body {
    font-family: "Open Sans";
}
body {
    background-color: #f4f4f4;
}
.credits {
    font-size: 0.8em;
    text-align: center;
}
.love {
    background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/42764/heart-smil.svg);
    display: inline-block;
    height: 16px;
    vertical-align: middle;
    width: 16px;
}
@-webkit-keyframes link {
    25% {
        -webkit-transform: rotate(10deg);
        transform: rotate(10deg);
    }
    50% {
        -webkit-transform: rotate(-10deg);
        transform: rotate(-10deg);
    }
}
@keyframes link {
    25% {
        -webkit-transform: rotate(10deg);
        transform: rotate(10deg);
    }
    50% {
        -webkit-transform: rotate(-10deg);
        transform: rotate(-10deg);
    }
}
</style>
