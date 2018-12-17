<template>
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
.head {
    position: relative;
    width: 50px;
}
.horns {
    -webkit-animation: rocking 0.4s cubic-bezier(0.4, 0, 0.2, 1) infinite
        alternate-reverse;
    animation: rocking 0.4s cubic-bezier(0.4, 0, 0.2, 1) infinite
        alternate-reverse;
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
    -webkit-animation: ear-left 2s cubic-bezier(0.6, -0.28, 0.74, 0.05) infinite
        alternate-reverse;
    animation: ear-left 2s cubic-bezier(0.6, -0.28, 0.74, 0.05) infinite
        alternate-reverse;
    -webkit-transform: rotate(30deg);
    transform: rotate(30deg);
}
.ear-right {
    -webkit-animation: ear-right 2s cubic-bezier(0.6, -0.28, 0.74, 0.05) 2s
        infinite alternate-reverse;
    animation: ear-right 2s cubic-bezier(0.6, -0.28, 0.74, 0.05) 2s infinite
        alternate-reverse;
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
</style>
