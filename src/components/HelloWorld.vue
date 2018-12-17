<template>
    <div class="container">
        <div class="artboard">
            <div class="deer">
                <div class="rocking">
                    <ElkHead/>
                    <ElkBody/>
                </div>
                <ElkTail/>
                <ElkLegs/>
            </div>
            <div class="presents">
                <!-- 红色 -->
                <Present
                    class="present present-one"
                    :size="45"
                    boxColor="#fb5d5d"
                    ribbonColor="transparent"
                />
                <Present class="present"/>
                <Present class="present present-two-right"/>
                <!-- 黄色 -->
                <Present
                    class="present present-three"
                    :size="25"
                    boxColor="#ffb63c"
                    ribbonColor="#fb5353"
                />
            </div>
            <SnowFlake count="50"/>
        </div>
    </div>
</template>

<script>
import SnowFlake from "./SnowFlake.vue";
import Present from "./Present.vue";
import ElkHead from "./ElkHead.vue";
import ElkBody from "./ElkBody.vue";
import ElkLegs from "./ElkLegs.vue";
import ElkTail from "./ElkTail.vue";

export default {
    name: "HelloWorld",
    components: {
        SnowFlake,
        Present,
        ElkHead,
        ElkBody,
        ElkLegs,
        ElkTail
    },
    props: {
        msg: String
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* @import url(https://fonts.googleapis.com/css?family=Open+Sans:400, 600); */
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
