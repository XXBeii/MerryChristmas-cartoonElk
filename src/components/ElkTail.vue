<template>
    <div class="tail">
        <div class="circle">
            <div class="circle">
                <div class="circle">
                    <div class="circle">
                        <div class="circle"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "ElkTail",
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
</style>
