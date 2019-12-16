<template>
  <div>
    <h1 class="title">My Blog App Amplify Test!!!!</h1>
    <ul>
      <li v-for='(post, index) in posts' :key='index'>
        <router-link :to="`/post/${post.id}`">{{post.title}}</router-link>
      </li>
    </ul>
  </div>
</template>
<script>
  export default {
    data(){
      return {}
    },
    computed:{
      posts(){
        return this.$store.state.posts
      }
    },
    mounted(){
      this.$store.dispatch("load")
    }
  }
</script>




<!--<template>-->
  <!--<div>-->
    <!--<h1 class="title">My Blog App</h1>-->
    <!--<h2></h2>-->
    <!--<ul>-->
      <!--<li v-for='(post, index) in posts' :key='index'>-->
      <!--&lt;!&ndash;indexは配列の位置(番号)を取ってくる。配列内のデータをすべて取りたいときは、-->
      <!--:key='index'としてなにかkeyを渡してあげる。&ndash;&gt;-->
      <!--<router-link :to="`/post/${post.id}`">{{post.title}}</router-link>-->
      <!--</li>-->
    <!--</ul>-->
  <!--</div>-->
<!--</template>-->


<!--<script>-->
  <!--export default{-->
    <!--data(){-->
      <!--return{}-->
    <!--},-->
    <!--computed: {-->
      <!--posts(){-->
        <!--return this.$store.state.posts-->
      <!--}-->
    <!--},-->
    <!--mounted() {-->
      <!--this.$store.dispatch("load")-->
    <!--},-->
    <!--// validate({params}){-->
    <!--//   // 投稿のスラッグは 英字 6文字。-->
    <!--//   //マッチしない文字列でアクセスした場合はエラーページが表示される。-->
    <!--//   return /^[a-z]{6}$/.test(params.slug)-->
    <!--// }-->
  <!--}-->
<!--</script>-->

<!--<style scoped>-->

  <!--.container {-->
    <!--min-height: 100vh;-->
    <!--display: flex;-->
    <!--justify-content: center;-->
    <!--align-items: center;-->
    <!--text-align: center;-->
  <!--}-->

  <!--.title {-->
    <!--font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */-->
    <!--display: block;-->
    <!--font-weight: 300;-->
    <!--font-size: 100px;-->
    <!--color: #35495e;-->
    <!--letter-spacing: 1px;-->
  <!--}-->

  <!--.subtitle {-->
    <!--font-weight: 300;-->
    <!--font-size: 42px;-->
    <!--color: #526488;-->
    <!--word-spacing: 5px;-->
    <!--padding-bottom: 15px;-->
  <!--}-->

  <!--.links {-->
    <!--padding-top: 15px;-->
  <!--}-->

  <!--.page-enter-active, .page-leave-active{-->
    <!--transition: opacity .5s;-->
  <!--}-->

  <!--.page-enter, .page-leave-to{-->
    <!--opacity: 0;-->
  <!--}-->
<!--</style>-->

