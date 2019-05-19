<template>
  <div class="text-xs-center">
    <app-toolbar></app-toolbar>
    <div class="url">
    <h1 style="color:indigo;" padding-top:135px>URL Extractor from PCAP files</h1>
    <v-dialog
      v-model="dialog"
      width="500"
    >
      <template v-slot:activator="{ on }">
        <v-btn
          color="red lighten-2"
          dark
          v-on="on"
          class="button2"
        >
          How to use 
        </v-btn>
      </template>

      <v-card>
        <v-card-title
          class="headline grey lighten-2"
          primary-title
        >
          Quick Tip
        </v-card-title>

        <v-card-text>
        Store Pcap file you want to extract with name extract.pcap in /Desktop/DMS/PCAP. Extracted data from pcap can be found in /Desktop/DMS/CSV
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="primary"
            flat
            @click="dialog = false"
          >
            I Got It
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
    <div>
      <form action="http://localhost:3800/extract">
      <v-btn type="submit" class="button2" color="green lighten-1" dark>Extract URL</v-btn>
      </form>
    </div>
    <app-footer></app-footer>
  </div>
  </div>
</template>

<script>
import AppFooter from './AppFooter'
import AppToolbar from './AppToolbar'

  export default {
    components: {AppFooter, AppToolbar},
    data () {
      return {
        dialog: false
      }
    }
  }
</script>

<style>
.button2 {
    width: 20%;
    height: 60px;
}

.url{
  margin-top: 120px;
}
</style>
