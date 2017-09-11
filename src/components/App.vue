<template>
  <div>
    <header class="site-header jumbotron">
      <div class="container">
        <div class="row">
          <div class="col-xs-12">
            <h1>请发表对React的评论</h1>
          </div>
        </div>
      </div>
    </header>
    <div class="container">
      <add :addComment="addComment"></add>
      <list :comments="comments"></list>
    </div>
  </div>
</template>

<script>
  import add from './Add.vue'
  import list from './List.vue'
  export default {
    data(){
        return{
           comments:[
               {name:'jack',content:'vue还不错'},
               {name:'Tom',content:'vue老是报错，真烦人！'}
               ]
        }
    },
    methods:{
        addComment(comment){
            this.comments.unshift(comment)
        }
    },
    components: {
        add,list
    }
  }
</script>

<style>

</style>
