<template>
    <div class="member">
        <div class="nav-header">
            <el-row type="flex"  :gutter="20">
                <el-col :span="4">
                    <el-input v-model="mobile" placeholder="请输入手机号"></el-input>
                </el-col>
                <el-col :span="4">
                    <el-input v-model="name" placeholder="请输入姓名"></el-input>
                </el-col>
                <el-col :span="4">
                    <el-button type='primary'  icon="el-icon-search" @click="getList">查询</el-button>
                </el-col>
            </el-row>    
        </div>
        <div class="content">
            <el-table :data="list"  v-loading="loading" style="width: 100%;" >
                <el-table-column type="index" width="50"></el-table-column>
                <el-table-column prop='name' label="姓名" width="150"></el-table-column>
                <el-table-column prop='mobile' label='手机' width="150"></el-table-column>
                <el-table-column prop='age' label='年龄' width="80"></el-table-column>
                <el-table-column prop="register_time" label="注册时间" min-width="150"></el-table-column>
                <el-table-column fixed="right" width="150" label="操作" >
                    <template slot-scope="scope">
                        <el-button size="mini" type="primary"  icon="el-icon-edit"></el-button>
                        <el-button size="mini" type="danger" icon="el-icon-delete"></el-button>
                    </template>
                </el-table-column>
            </el-table>  
            <div class="page-wrapper">
                <el-pagination layout="prev, pager, next" :total="total" @current-change='changePage'></el-pagination>
            </div>  
        </div>
    </div>
</template>

<script>
import { MEMBER_LIST } from '@/api'

export default {
    data(){
        return {
            mobile:'',
            name:'',
            total:0,
            page:1,
            list:[],
            loading: true,
        }
    },
    methods:{
        // 获取列表
        getList(){
            this.loading = true
            MEMBER_LIST().then(res=>{
                this.loading = false
                if(res.data.code === 200){
                    this.total = res.data.data.total
                    this.list = res.data.data.data
                }
            })
        },

        // 翻页
        changePage(page){
            this.page = page
            this.getList()
        }
        
    },
    created(){
        this.getList()
    }

}
</script>

<style scoped>

</style>

