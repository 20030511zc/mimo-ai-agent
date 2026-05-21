<template>
  <div>
    <h2 class="page-title">智能调试助手</h2>
    
    <el-card>
      <el-form label-width="100px">
        <el-form-item label="错误信息">
          <el-input 
            v-model="error" 
            type="textarea" 
            :rows="4" 
            placeholder="例如：Uncaught TypeError: Cannot read property 'length' of undefined"
          />
        </el-form-item>
        <el-form-item>
          <el-button type="primary" @click="analyzeError">智能分析</el-button>
        </el-form-item>
      </el-form>
      
      <el-alert 
        v-if="solution" 
        title="解决方案" 
        type="info" 
        :closable="false"
        style="margin-top: 20px"
      >
        <p>{{ solution }}</p>
        <p>支持HTML、CSS、JavaScript、Vue、React等多种前端技术栈的调试。</p>
      </el-alert>
    </el-card>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const error = ref('')
const solution = ref('')

const analyzeError = () => {
  if (!error.value) return
  solution.value = 'MiMo大模型正在分析你的错误信息，将提供详细的解决方案和修复代码。'
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