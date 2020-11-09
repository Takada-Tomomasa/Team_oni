<template>
  <div class="home">
    <div class="title">
      HOME
    </div>
    <button class="go-to-next" @click="nextPage">
      開始する
    </button>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'Index',
  methods: {
    nextPage (): void {
      this.$router.push('./ApplicationMainPage')
    }
  }
})
</script>

<style scoped>
.title{
  font-size: 150%;
}
</style>
