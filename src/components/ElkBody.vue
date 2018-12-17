<template>
    <div class="body">
        <div class="shadow"></div>
        <div class="hooves">
            <div class="hoof-one">
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
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "ElkBody",
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
</style>
