<template>
  <div class="container">
    <div class="title">
      アプリのメインページ
    </div>
    <p>ここに色々実験していこう！</p>
    <p>{{ message }}</p>
    <input v-model="commentNumber">
    <button @click="findBody">
      検索
    </button>
    <p>{{ commentData[commentNumber] }}</p>
    <Todos :comment-number="commentNumber" />
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
      commentNumber: null,
      message: ''
    }
  },
  mounted () {
    fetch('https://jsonplaceholder.typicode.com/comments')
      .then(response => response.json())
      .then(json => (this.commentData = json))
  },
  methods: {
    findBody () {
      this.$router.push('./findBodyPage?commentNumber=' + this.commentNumber)
    }
  }
}
</script>

<style scoped>
.container {
  text-align: center;
}

</style>
