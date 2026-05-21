<template>
  <div>
    <h2 class="page-title">欢迎使用 MiMo AI 智能开发系统</h2>

    <div class="stats-grid">
      <div class="stat-card">
        <div class="stat-value">78%</div>
        <div class="stat-label">开发效率提升</div>
      </div>
      <div class="stat-card">
        <div class="stat-value">2500+</div>
        <div class="stat-label">已生成代码行数</div>
      </div>
      <div class="stat-card">
        <div class="stat-value">92%</div>
        <div class="stat-label">代码准确率</div>
      </div>
      <div class="stat-card">
        <div class="stat-value">8.6万</div>
        <div class="stat-label">累计Token消耗</div>
      </div>
    </div>

    <div class="feature-card">
      <h3 class="feature-title">项目核心功能</h3>
      <p class="feature-desc">
        本系统是基于小米MiMo大模型构建的前端智能开发Agent，专为企业级后台管理系统开发设计。
        具备长链推理、多轮迭代调试、代码自动生成、样式自适应优化、兼容性自动排查等核心能力，
        可大幅缩短前端开发周期，降低开发门槛。
      </p>
    </div>

    <div class="feature-card">
      <h3 class="feature-title">MiMo模型应用场景</h3>
      <p class="feature-desc">
        1. 自动生成完整的后台布局与组件代码<br>
        2. 智能优化CSS样式与响应式适配<br>
        3. 多轮迭代调试代码错误与逻辑问题<br>
        4. 根据需求自动扩展功能模块<br>
        5. 生成符合规范的代码注释与文档
      </p>
    </div>
  </div>
</template>

<style scoped>
.page-title {
  font-size: 24px;
  font-weight: 600;
  color: #1E293B;
  margin-bottom: 24px;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  margin-bottom: 24px;
}

.stat-card {
  background: white;
  padding: 20px;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
}

.stat-value {
  font-size: 28px;
  font-weight: 700;
  color: #165DFF;
  margin-bottom: 4px;
}

.stat-label {
  font-size: 14px;
  color: #64748B;
}

.feature-card {
  background: white;
  padding: 24px;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
  margin-bottom: 20px;
}

.feature-title {
  font-size: 18px;
  font-weight: 600;
  color: #1E293B;
  margin-bottom: 12px;
}

.feature-desc {
  color: #64748B;
  line-height: 1.6;
}
</style>