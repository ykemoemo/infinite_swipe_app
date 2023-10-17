<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to the Vuetify 3 Beta
        </h1>
      </v-col>
    </v-row>
    <v-card
      v-touch="{
        up: function(){swipeObserve('上方向')},
        right: function(){swipeObserve('右方向')},
        down: function(){swipeObserve('下方向')},
        left: function(){swipeObserve('左方向')}
      }"
      height="200"
      width="200"
      elevation="3"
    >
      スワイプの向き：{{direction}}
    </v-card>
  </v-container>
</template>

<script>

export default {
  name: 'HelloWorld',

  methods: {
    swipeObserve(e) {
      this.direction = e;
    }
  },

  data: () => ({
    direction: '',
    // ...(他のdata)...
  }),
}
</script>
