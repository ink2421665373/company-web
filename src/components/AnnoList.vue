<template>
<div class="notice-list">
    <h1 class="page-title">公告列表</h1>
    <el-table :data="notices" height="500" border style="width: 100%">
        <el-table-column prop="title" label="标题" style="width: 20px;"></el-table-column>
        <el-table-column prop="content" label="公告内容" width=""></el-table-column>
        <el-table-column label="操作"  >
        <template slot-scope="scope">
            <el-button type="primary" size="small" @click="editNotice(scope.row)">修改</el-button>
            <el-button type="danger" size="small" @click="deleteNotice(scope.row)">删除</el-button>
        </template>
        </el-table-column>
    </el-table>
    </div>
</template>

<script>
export default {
    name:'AnnoList',
    data() {
    return {
        notices: [
        { title: '公告1', content: '公告内容1' },
        { title: '公告2', content: '公告内容2' },
        { title: '公告3', content: '公告内容3' },
        { title: '公告4', content: '公告内容4' },
        { title: '公告5', content: '公告内容5' },
        { title: '公告6', content: '公告内容6' },
        ],
    };
    },
    methods: {
    editNotice(notice) {
      // 执行编辑公告的逻辑，例如跳转到编辑页面
    console.log('编辑公告', notice);
    },
    deleteNotice(notice) {
      // 执行删除公告的逻辑，例如弹出确认框后发送请求删除公告
    console.log('删除公告', notice);
    },
    },
};
</script>

<style>
.page-title {
    font-size: 24px;
    margin-bottom: 20px;
}

.notice-list {
    max-width: 100%;
    /* margin: 0 auto; */
    padding: 20px;
}

/* Clov614修改样式 */
el-table {
    display: flex;
}
</style>
