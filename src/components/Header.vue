<template>
  <header class="header">
    <div class="container header-content">
      <div class="logo">
        <h1>瑛鼎</h1>
        <p class="company-name">东莞市瑛鼎塑胶制品有限公司</p>
        <p class="slogan">专业皮革贸易 · 耳机皮套 · 负氧离子革</p>
      </div>
      <div class="contact-info">
        <p><strong>电话：</strong> 18578038023</p>
        <p><strong>邮箱：</strong> 1770706657@qq.com</p>
        <p><strong>地址：</strong> 广东省东莞市</p>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
.header {
  background: linear-gradient(135deg, var(--primary-color) 0%, #a01530 100%);
  color: white;
  padding: 40px 20px;
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 40px;
}

.logo h1 {
  font-size: 3rem;
  font-weight: bold;
  margin-bottom: 10px;
  color: white;
}

.company-name {
  font-size: 1.1rem;
  margin-bottom: 5px;
  font-weight: 500;
}

.slogan {
  font-size: 0.95rem;
  opacity: 0.9;
  letter-spacing: 1px;
}

.contact-info p {
  margin: 8px 0;
  font-size: 0.95rem;
}

.contact-info strong {
  color: var(--accent-color);
}

@media (max-width: 768px) {
  .header-content {
    flex-direction: column;
    text-align: center;
  }
  
  .logo h1 {
    font-size: 2rem;
  }
}
</style>
