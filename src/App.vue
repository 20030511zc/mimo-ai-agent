<template>
  <div class="app">
    <!-- 顶部导航栏 -->
    <div class="header">
      <div class="header-left">
        <div class="logo">AI</div>
        <h1 class="header-title">MiMo AI 前端智能开发Agent</h1>
        <span class="ai-badge">v1.0 正式版</span>
      </div>
      <div>基于小米MiMo大模型驱动</div>
    </div>

    <!-- 主体区域 -->
    <div class="main">
      <!-- 侧边栏 -->
      <div class="sidebar">
        <div 
          v-for="(item, index) in menuList" 
          :key="index"
          class="menu-item"
          :class="{ active: $route.path === item.path }"
          @click="$router.push(item.path)"
        >
          <span>{{ item.icon }}</span>
          <span>{{ item.name }}</span>
        </div>
      </div>

      <!-- 主内容区 -->
      <div class="content">
        <router-view />
      </div>
    </div>
  </div>
</template>

<script setup>
const menuList = [
  { name: '数据看板', path: '/', icon: '📊' },
  { name: '用户管理', path: '/users', icon: '👤' },
  { name: 'AI代码生成', path: '/codegen', icon: '💻' },
  { name: '智能调试', path: '/debug', icon: '🔧' },
  { name: '系统设置', path: '/settings', icon: '⚙️' }
]
</script>

<style scoped>
.app {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  background-color: #f5f7fa;
  font-family: "Inter", "Microsoft YaHei", sans-serif;
}

.header {
  height: 64px;
  background: linear-gradient(135deg, #165DFF 0%, #4080FF 100%);
  color: white;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 24px;
  box-shadow: 0 2px 12px rgba(22, 93, 255, 0.15);
}

.header-left {
  display: flex;
  align-items: center;
  gap: 12px;
}

.logo {
  width: 32px;
  height: 32px;
  background: white;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  color: #165DFF;
}

.header-title {
  font-size: 18px;
  font-weight: 600;
}

.ai-badge {
  background: rgba(255, 255, 255, 0.2);
  padding: 4px 10px;
  border-radius: 12px;
  font-size: 12px;
  margin-left: 8px;
}

.main {
  display: flex;
  flex: 1;
}

.sidebar {
  width: 240px;
  background: #0F172A;
  color: #CBD5E1;
  padding-top: 16px;
}

.menu-item {
  height: 52px;
  display: flex;
  align-items: center;
  padding: 0 24px;
  cursor: pointer;
  transition: all 0.2s ease;
  border-left: 3px solid transparent;
}

.menu-item:hover, .menu-item.active {
  background: #1E293B;
  color: #409EFF;
  border-left-color: #409EFF;
}

.menu-item span {
  margin-left: 12px;
}

.content {
  flex: 1;
  padding: 24px;
  overflow-y: auto;
}
</style>