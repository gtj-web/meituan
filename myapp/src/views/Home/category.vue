<template>
    <div>
        <ul class="cate-box">
            <li class="cate-list" v-for="obj in cateList" :key="obj.id">
                <img class="cate-img" :src="obj.img" alt="">
                <p class="cate-title">{{obj.name}}</p>
            </li>
        </ul>
    </div>
</template>

<script>
import {getCategory} from '@/api/home.js'
    export default {
        data(){
            return {
                cateList:[]
            }
        },
        created() {
            getCategory().then(res=>{
                this.cateList = res.data;
            })
        },
    }
</script>

<style lang="scss" scoped>
    .cate-box{
        display: flex;
        flex-wrap: wrap;
        .cate-list{
            width: 20%;
            text-align: center;
            padding-top: 0.3rem;
            font-size: 13px;
            .cate-img{
                width: 0.88rem;
                height: 0.88rem;
                padding-bottom: 0.05rem;
            }
        }
    }
</style>