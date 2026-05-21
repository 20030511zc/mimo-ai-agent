<template>
  <div>
    <h2 class="page-title">AI代码生成器</h2>
    
    <el-card>
      <el-form label-width="100px">
        <el-form-item label="需求描述">
          <el-input 
            v-model="prompt" 
            type="textarea" 
            :rows="4" 
            placeholder="例如：生成一个带搜索和分页功能的用户列表表格"
          />
        </el-form-item>
        <el-form-item>
          <el-button type="primary" @click="generateCode">生成代码</el-button>
        </el-form-item>
      </el-form>
      
      <div class="code-output" v-if="code">
        <pre>{{ code }}</pre>
      </div>
    </el-card>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const prompt = ref('')
const code = ref('')

const generateCode = () => {
  if (!prompt.value) return
  code.value = `// 基于MiMo大模型生成的代码
// 需求：${prompt.value}
// 自动适配响应式布局
// 包含完整的样式和交互逻辑

<template>
  <div class="component">
    <!-- 组件内容 -->
  </div>
</template>

<script setup>
// 组件逻辑
<\/script>

<style scoped>
/* 组件样式 */
</style>`
}
</script>

<style scoped>
.page-title {
  font-size: 24px;
  font-weight: 600;
  color: #1E293B;
  margin-bottom: 24px;
}

.code-output {
  margin-top: 20px;
  background: #0F172A;
  color: #E2E8F0;
  padding: 20px;
  border-radius: 8px;
  overflow-x: auto;
}

.code-output pre {
  white-space: pre-wrap;
  font-family: monospace;
}
</style>