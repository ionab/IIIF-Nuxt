<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <v-card>
        <OpenSeaDragon />
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import OpenSeaDragon from '~/components/OpenSeaDragon.vue'

export default {
  components: {
    OpenSeaDragon
  }
}
</script>
