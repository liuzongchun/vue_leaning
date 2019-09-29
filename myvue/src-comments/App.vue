<template>
  <div>
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
        <Add :addComment="addComment"/>
        <List :comments='comments' :removeComment="removeComment"/>
<!--        组件间通信-->
      </div>
    </div>
  </div>
</template>

<script>
    import Add from './components/Add'
    import List from './components/List.vue'

    export default {
        data(){
            return {
                comments:[{
                    name:'cat',
                    content:'Vue good'
                },{
                    name:'tom',
                    content:'Vue so easy'
                },{
                    name:'jc',
                    content:'Vue so so'
                }]
            }

        },
        methods:{
            addComment(comment){
                this.comments.unshift(comment)
            },
            removeComment(index){
                this.comments.splice(index,1)
            }
        },
        components: {
            Add, List
        }
    }
</script>

<style>
</style>
