<template>
  <v-ons-page>
    <v-ons-toolbar>
      <div class="left">
        <v-ons-toolbar-button>
          <v-ons-icon icon="ion-more, material:md-more-vert"></v-ons-icon>
        </v-ons-toolbar-button>
      </div>
      <div class="center">Naslov</div>
    </v-ons-toolbar>
    <div class="center">
      <v-ons-list>
        <v-ons-list-header>Naslov liste</v-ons-list-header>
        <v-ons-list-item>Prvi</v-ons-list-item>
      </v-ons-list>
      <v-ons-button @click="goHome">Go Home</v-ons-button>
    </div>
  </v-ons-page>
</template>

<script>
import Home from './Home'

export default {
  methods: {
      goHome(){
          this.$emit('push-page', {
              ...Home,
              props: {
                  name: 'Maja'
              }
          })
      }
  }
}
</script>



