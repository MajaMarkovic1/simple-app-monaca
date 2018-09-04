<template>
  <v-ons-navigator 
  :page-stack="pageStack"
  @push-page="pushPage">
  </v-ons-navigator>
</template>

<script>
import Nav from './Nav'

export default {
  data(){
    return {
      pageStack: [ Nav ],
      options: {
        animation: 'fade',
        animationOptions: {
          duration: 3
        }
      }
    }
  },
  methods: {
    pushPage(page){
      this.pageStack.push(page)
    }
  }
  
}
</script>

