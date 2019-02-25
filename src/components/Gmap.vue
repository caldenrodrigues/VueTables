<template lang="html">
  <div>
    <v-btn
              fixed
              dark
              fab
              bottom
              right
              color="green accent-4"
              @click="dialog = true"
            >
              <v-icon style="height: auto">map</v-icon>
    </v-btn>

    <v-dialog
        v-model="dialog"
        max-width="1000"
      >
        <v-card>
          <v-card-title class="headline">Location</v-card-title>

          <v-card-text>
            <GmapMap v-bind:center="center" v-bind:zoom="7"
            style="height: 500px">
              <GmapMarker
              v-bind:key="index"
              v-for="(m,index) in markers"
              v-bind:position="m.position"
              v-bind:clickable="true"
              v-bind:draggable="true"
              @click="center=m.position">
              </GmapMarker>
            </GmapMap>
          </v-card-text>

          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn
              color="green darken-1"
              flat="flat"
              @click="dialog = false"
            >
              Cool
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>


  </div>
</template>

<script>
export default {
  name: "Gmap",
  data() {
    return {
      center: {lat:62.0, lng:10.0},
      markers: [
        {
          position: {lat: 62.0, lng: 10.0}
        },
        {
          position: {lat: 63.0, lng:11.0}

        }
      ],
      dialog: false
    }
  }
}
</script>

<style lang="css" scoped>
</style>
