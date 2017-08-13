<template>
  <div id="">
    <v-container fluid fill-height>
      <v-layout row wrap>
        <v-flex xs12>
          <v-card fluid>
            <v-card-title primary-title>
              <div>
                <h1 class="display-4 fluid">{{card_heading}}</h1>
                <!--<p class="mt-4">{{card_text}}</p>-->
              </div>
            </v-card-title>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        card_heading: 'Comming Soon...',
        card_text: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.'
      }
    }
  }
</script>

<style scoped>
  h1 {
    color: white;
  }
</style>
