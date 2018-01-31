<template>
  <baidu-map class="map" :center="{lng: 116.404, lat: 39.915}" :zoom="15" :mapStyle="{styleJson: styleJson}">
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
        ]
      }
    }
  }

</script>
