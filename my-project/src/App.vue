<template>
    <baidu-map class="map" :center="{lng: 116.404, lat: 39.915}" :zoom="15" :scroll-wheel-zoom="true">

        <bm-point-collection :points="points" :color="points.status=='completed'?'red':'blue'"></bm-point-collection>



    </baidu-map>
</template>
<script>
    export default {
        data() {
            return {
                points: [{
                    lng: 116.381,
                    lat: 39.901,
                    status: 'a'
                }, {
                    lng: 116.382,

                    lat: 39.902,

                    status: 'completed'
                }, {
                    lng: 116.383,

                    lat: 39.903,

                    status: 'completed'
                }]

            }
        },
        methods: {

        },
        mounted() {

        }
    }

</script>
<style>
    .map {
        width: 900px;
        height: 900px
    }

</style>
