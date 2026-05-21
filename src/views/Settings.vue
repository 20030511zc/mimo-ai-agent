<template>
  <div>
    <h2 class="page-title">系统设置</h2>
    
    <el-card>
      <el-form label-width="120px">
        <el-form-item label="模型选择">
          <el-select v-model="settings.model" style="width: 200px">
            <el-option label="MiMo-7B" value="mimo-7b" />
            <el-option label="MiMo-13B" value="mimo-13b" />
            <el-option label="MiMo-34B" value="mimo-34b" />
          </el-select>
        </el-form-item>
        
        <el-form-item label="代码风格">
          <el-select v-model="settings.style" style="width: 200px">
            <el-option label="标准风格" value="standard" />
            <el-option label="Airbnb风格" value="airbnb" />
            <el-option label="Google风格" value="google" />
          </el-select>
        </el-form-item>
        
        <el-form-item label="自动保存">
          <el-switch v-model="settings.autoSave" />
        </el-form-item>
        
        <el-form-item label="响应式适配">
          <el-switch v-model="settings.responsive" />
        </el-form-item>
        
        <el-form-item>
          <el-button type="primary" @click="saveSettings">保存设置</el-button>
        </el-form-item>
      </el-form>
    </el-card>
  </div>
</template>

<script setup>
import { reactive } from 'vue'
import { ElMessage } from 'element-plus'

const settings = reactive({
  model: 'mimo-13b',
  style: 'standard',
  autoSave: true,
  responsive: true
})

const saveSettings = () => {
  ElMessage.success('设置保存成功')
}
</script>

<style scoped>
.page-title {
  font-size: 24px;
  font-weight: 600;
  color: #1E293B;
  margin-bottom: 24px;
}
</style>