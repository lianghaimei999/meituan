<template>
    <div>
       <!-- header -->
       <van-sticky :offset-top="0">
            <div class="header">
                <input type="text" class="search" placeholder="请输入商家或商品名称">
            </div>
       </van-sticky>
       <!-- 列表子组件 -->
       <categroy></categroy>
       <!-- 附近商家 -->
       <div class="title">附近商家</div>
       <!-- 列表子组件 -->
       <list></list>
    </div>
</template>
<script>
    //引入子组件
    import categroy from './category'
    import list from './list'
    export default{
        //引入子组件后声明
        components:{
            categroy,
            list
        },
        methods:{
           
        }
    }
</script>

<style lang="scss" scoped>
    .header{
        background-color: rgb(255, 204, 51);
        padding: 0.2rem;
        .search{
            width: 100%;
            border: none;
            height: 0.6rem;
            line-clamp: 0.6rem;
            border-radius: 0.3rem;
            padding: 0 0.2rem;
            box-sizing: border-box;
        }
    }
    .title{
        font-size: 0.34rem;
        font-weight: 800;
        text-align: center;
        height: 0.46rem;
        line-height: 0.46rem;
        margin:  0.3rem 0 0.1rem;
    }
    .title::before,.title::after{
        content: "";
        height: 1px;
        transform: scaleY(0.5);//为了解决height: 1px;变成2px
        width: 30px;
        display: inline-block;
        background: #999;
        vertical-align: middle;
    }
</style>