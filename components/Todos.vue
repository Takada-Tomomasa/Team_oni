<template>
  <div class="oni-todos">
    <h1>明後日までに学びたいこと</h1>
    <h3>{{ cdata }}</h3>
    <!-- <input v-model="number"> -->
    <ul>
      <li>アプリのフォルダ構成について(何をするときにどこをいじるか？)</li>
      <li>Vueの基本の確認(scriptの部分は全部tsで書く)</li>
      <ol>
        <li>v-if, v-for, v-on</li>
        <li>computed, methods</li>
        <li>v-model form入力</li>
        <li>component間の値の受け渡し</li>
        <li>(優先度低) testの書き方</li>
      </ol>
      <li>styleの書き方 ← 言われてないけど一番大事な気がする</li>
      <li>(優先度低) Gitでの資源管理</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Todos',
  props: {
    cdata: Object
  }
}
</script>

<style scoped>
.oni-todos{
  text-align: left;
  background-color:lightpink;
  margin-left: 400px;
  margin-right: 400px;
}
ul li {
  list-style-type: disc;
}
ol li {
  border-left: solid 6px #2d8fdd;
  list-style-type: none!important;
  padding: 0.2em;
}

</style>
