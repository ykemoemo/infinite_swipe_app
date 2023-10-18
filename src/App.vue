<template>
  <v-app style="text-align: center;">
    <h1>無限スワイプ</h1>
    <v-main>
      <HelloWorld/>
    </v-main>
    <h2>スワイプしすぎて指紋なくなる!!</h2>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
}
</script>
