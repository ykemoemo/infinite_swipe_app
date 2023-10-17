<template>
  <v-app>
    <h1>ヘッダー</h1>
    <v-main>
      <HelloWorld/>
    </v-main>
    <h1>フッター</h1>
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
