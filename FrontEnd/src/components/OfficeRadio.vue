<!--Todo : Fix import issues-->
<template>
  <v-container>
<!--    <v-layout-->
<!--      text-center-->
<!--      wrap-->
<!--    >-->
      <v-data-table
              :headers="headers"
              :items="songs"
              :items-per-page="15"
              class="elevation-1"
      >
        <template v-slot:item.action="{ item }">
          <v-icon
                  small
                  class="mr-2"

          >
           mdi-cards-heart
          </v-icon>
        </template>

      </v-data-table>
<!--    </v-layout>-->
  </v-container>
</template>

<script>
  import Papa from "papaparse"
export default {
  name: 'OfficeRadio',
  data: () => ({
    headers: [
      {
        text: 'Song',
        align: 'left',
        sortable: true,
        value: 'song',
      },
      {text: 'Artist', value: 'artist'},
      {text: 'Actions', value: 'action',sortable:false}
    ],
    songs: []

  })
  ,
  mounted: function(){
    var ref = this;
    Papa.parse("data/chart2000-song-2010-decade-0-3-0057.csv",{download:true,header:true,complete:function(results){
      console.log(results['data'])
      ref.songs=results['data'].slice(0)

    }})
  }
};
</script>
