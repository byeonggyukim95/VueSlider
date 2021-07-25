<template>
    <div class="slider">
        <div class="slider-item" :key="index" v-for="(data, index) in silderNum" :style="{background : data.color}"
            @mousedown="sliderDown"
            @mouseup="sliderUp"
            @mousemove="sliderMove"
            >
            {{data.color}}
        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                silderNum: [{
                        number: 1,
                        color: 'red'
                    },
                    {
                        number: 2,
                        color: 'yellow'
                    },
                    {
                        number: 3,
                        color: 'green'
                    }
                ]
            }
        },
        methods: {
            sliderDown() {
                let target = event.target;
                target.classList.add('active');
            },
            sliderUp() {
                let target = event.target;
                target.classList.remove('active');
            },
            sliderMove() {

            }
        }
    }
</script>