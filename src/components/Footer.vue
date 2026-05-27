<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-grid">
        <div class="footer-section">
          <h3>关于我们</h3>
          <p>
            东莞市瑛鼎塑胶制品有限公司专注皮革贸易与功能革应用，为全球客户提供专业的皮革解决方案。
          </p>
        </div>
        <div class="footer-section">
          <h3>产品服务</h3>
          <ul>
            <li><a href="#products">耳机皮套专用革</a></li>
            <li><a href="#products">负氧离子功能革</a></li>
            <li><a href="#products">皮革贸易配送</a></li>
            <li><a href="#products">深加工协同</a></li>
          </ul>
        </div>
        <div class="footer-section">
          <h3>联系方式</h3>
          <ul>
            <li>📞 18578038023</li>
            <li>📧 1770706657@qq.com</li>
            <li>🌐 www.yingding-leather.com</li>
            <li>📍 广东省东莞市</li>
          </ul>
        </div>
        <div class="footer-section">
          <h3>快速链接</h3>
          <ul>
            <li><a href="#about">公司简介</a></li>
            <li><a href="#advantages">核心优势</a></li>
            <li><a href="#contact">在线咨询</a></li>
            <li><a href="#home">返回顶部</a></li>
          </ul>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2024 东莞市瑛鼎塑胶制品有限公司 版权所有 | All Rights Reserved</p>
        <p>粤ICP备XXXXXXX号 | 隐私政策 | 使用条款</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
.footer {
  background-color: var(--secondary-color);
  color: #fff;
  padding: 50px 20px 20px;
  margin-top: auto;
}

.footer-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 40px;
  margin-bottom: 40px;
}

.footer-section h3 {
  color: var(--accent-color);
  margin-bottom: 15px;
  font-size: 1.1rem;
}

.footer-section p,
.footer-section li {
  color: #ddd;
  margin: 8px 0;
  line-height: 1.8;
}

.footer-section ul {
  list-style: none;
}

.footer-section a {
  color: #ddd;
  transition: color 0.3s ease;
}

.footer-section a:hover {
  color: var(--accent-color);
}

.footer-bottom {
  text-align: center;
  padding-top: 20px;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  color: #aaa;
  font-size: 0.9rem;
}

.footer-bottom p {
  margin: 5px 0;
}

@media (max-width: 768px) {
  .footer-grid {
    gap: 30px;
  }
}
</style>
