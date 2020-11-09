<template>
  <div class="container">
    <div class="title">
      アプリのメインページ
    </div>
    <p>ここに色々実験していこう！</p>
    <input v-model="commentNumber">
    <p>{{ commentData[commentNumber] }}</p>
    <Todos :commentData="cdata" />
    <!-- <Generic /> -->
  </div>
</template>

<script>
import Todos from '../components/Todos'

export default {
  name: 'ApplicationMainPage',
  components: {
    Todos
  },
  data () {
    return {
      commentData: [],
      commentNumber: null
    }
  },

  mounted () {
    fetch('https://jsonplaceholder.typicode.com/comments')
      .then(response => response.json())
      .then(json => (this.commentData = json))
  }
}
</script>

<style scoped>
.container {
  text-align: center;
}

</style>
