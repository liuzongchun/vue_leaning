<template>
  <li class="list-group-item">
    <div class="handle">
      <a href="javascript:;" @click="removeItem">删除</a>
    </div>
    <p class="user"><span >{{comment.name}}</span><span>说:</span></p>
    <p class="centence">{{comment.content}}</p>
  </li>
</template>

<script>
    export default {
        // props:['comment']//只指定属性名
        props:{//只指定属性名和属性值的类型
            comment:Object,
            removeComment:Function,
            index:Number
        },
        methods:{
            removeItem(){
                const {comment,index,removeComment} = this
                if(window.confirm(`确定删除${comment.name}的评论吗？`)){
                    removeComment(index)

                }
            }
        }
    }
</script>
<style>

</style>
