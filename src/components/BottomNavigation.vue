<template>
  <v-card flat style="bottom:0px;position:fixed;width:100%">
    <!-- <div class="headline text-xs-center pa-5">Active: {{ e1 }}</div> -->
    <v-bottom-nav dark fixed app absolute :value="true" :active.sync="e1" color="black">
      <v-btn flat color="teal" value="recent">
        <span>Recent</span>
        <v-icon>history</v-icon>
      </v-btn>
      <v-btn flat color="teal" value="favorites">
        <span>Favorites</span>
        <v-icon>favorite</v-icon>
      </v-btn>
      <v-btn flat color="teal" value="nearby">
        <span>Nearby</span>
        <v-icon>place</v-icon>
      </v-btn>
      <!-- Bottom Sheet -->
      <v-btn flat color="teal" value="compare">
        <span>Compare</span>
        <v-icon>compare</v-icon>
      </v-btn>
      <!-- <sheet /> -->
    </v-bottom-nav>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        e1: 'recent'
      }
    }
  }
</script>