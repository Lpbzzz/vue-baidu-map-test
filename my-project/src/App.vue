<template>
    <baidu-map class="map" :center="{lng: 116.404, lat: 39.915}" :zoom="15" :mapStyle="{styleJson: styleJson}">
      <bm-point-collection :points="points" color="red"></bm-point-collection>
    </baidu-map>
</template>
<script>
  export default {
    data() {
      return {
        styleJson: [{
            "featureType": "all",
            "elementType": "geometry",
            "stylers": {
              "hue": "#007fff",
              "saturation": 89
            }
          },
          {
            "featureType": "water",
            "elementType": "all",
            "stylers": {
              "color": "#ffffff"
            }
          }
        ],
        points: [{
          lng:116.407,
          lat:39.915
        }],
        pLng:116.405,
        pLat:39.914,
      }
    },
    methods: {
      addP(){
        this.pLat+=0.01;
        this.pLng+=0.01;
        let obj = {};
        obj.lng = this.pLng;
        obj.lat = this.pLat
        this.points.push(obj)
      }
    },
    mounted() {
      setInterval(e=>{
        this.addP()
      },1000)
    }
  }

</script>
<style>
  .map {
    width: 900px;
    height: 900px
  }

</style>
