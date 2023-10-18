<template>
  <v-container>
    <v-card
      v-touch="{
        up: function(){superLike(superLikeCount += 1)},
        right: function(){like(likeCount += 1)},
        down: function(){superNope(superNopeCount += 1)},
        left: function(){nope(nopeCount += 1)}
      }"
      height="500"
      width="300"
      elevation="3"
      style="margin: 0 auto;
             margin-top: 20px;
             margin-bottom: 20px;"
    >
    </v-card>
    <div style="text-align: center;">
      スーパーライク数：{{superLikeCount}}<br>
      ライク数：{{likeCount}}<br>
      スーパーノープ数：{{superNopeCount}}<br>
      ノープカウント数：{{nopeCount}}
    </div>
  </v-container>
</template>

<script>
export default {
  name: 'HelloWorld',

  methods: {
    superLike(e) {
      this.superLikeCount = e;
    },
    like(e) {
      this.likeCount = e;
    },
    superNope(e) {
      this.superNopeCount = e;
    },
    nope(e) {
      this.nopeCount = e;
    }
  },

  data: () => ({
    superLikeCount: 0,
    likeCount: 0,
    superNopeCount: 0,
    nopeCount: 0,
  })
}
</script>
