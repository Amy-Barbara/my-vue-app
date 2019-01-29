<template>
    <div>
        <article v-if="post">
    <h1 class="title">{{post.title}}</h1>
        <p>ここに記事の本文が入ります。</p>
        </article>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                post: null
            }
        },
        mounted() {
            for(let post of this.$store.state.posts){
                if(post.id == this.$route.param.id){
                    this.post = post
                }
            }
            if(!this.post){
                //記事が存在しない場合はトップへ
                this.$router.push("/")
            }
        }
    }

</script>

<style>

</style>