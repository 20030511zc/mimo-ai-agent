<template>
  <div>
    <h2 class="page-title">用户管理</h2>
    
    <el-table :data="userList" border stripe style="width: 100%">
      <el-table-column prop="username" label="用户名" />
      <el-table-column prop="email" label="邮箱" />
      <el-table-column prop="role" label="角色" />
      <el-table-column prop="createTime" label="注册时间" />
      <el-table-column label="操作">
        <template #default="scope">
          <el-button type="primary" size="small">编辑</el-button>
          <el-button type="danger" size="small" v-if="scope.row.role !== '管理员'">删除</el-button>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>

<script setup>
const userList = [
  { username: 'admin', email: 'admin@example.com', role: '管理员', createTime: '2024-01-15' },
  { username: 'user01', email: 'user01@example.com', role: '普通用户', createTime: '2024-02-20' },
  { username: 'user02', email: 'user02@example.com', role: '普通用户', createTime: '2024-03-05' },
  { username: 'developer', email: 'dev@example.com', role: '开发者', createTime: '2024-03-10' }
]
</script>

<style scoped>
.page-title {
  font-size: 24px;
  font-weight: 600;
  color: #1E293B;
  margin-bottom: 24px;
}
</style>