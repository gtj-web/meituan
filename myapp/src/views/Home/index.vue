<template>
    <div>
        <van-sticky :offset-top="0">
            <!-- header -->
            <div class="header">
                <input type="text" class="search" placeholder="请输入商家或商品名称">
            </div>
        </van-sticky>
        <category></category>
        <div class="title">附近商家</div>
        <list></list>
    </div>
</template>

<script>
import category from './category'
import list from './list'

    export default {
        components:{
            category,
            list
        }
    }
</script>

<style lang="scss" scoped>
    .header{
        background: #1c1b20;
        padding: 0.2rem;
        .search{
            width: 100%;
            border:none;
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
        margin: 0.3rem 0 0.1rem;
    }
    .title::after,.title::before{
        content: "";
        height: 1px;
        transform: scaleY(0.5);
        width: 30px;
        display: inline-block;
        background-color: #666;
        vertical-align: middle;
    }
</style>