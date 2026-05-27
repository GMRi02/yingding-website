<template>
  <section id="about" class="about-section section">
    <div class="container">
      <h2 class="section-title">公司简介</h2>
      
      <div class="about-content">
        <div class="about-text">
          <p>
            东莞市瑛鼎塑胶制品有限公司扎根中国皮革产业重镇——广东东莞，
            是一家以皮革贸易为核心、深耕消费电子配件革料及功能性皮革研发推广的专业企业。
          </p>
          <p>
            公司主营耳机皮套（耳罩皮、头梁皮、收纳包皮等）用革，
            以及负氧离子革等具有健康理念的功能性皮革材料，
            为耳机品牌商、ODM工厂、皮具加工厂及贸易公司提供稳定货源、专业选皮与快速交付服务。
          </p>
          <p>
            依托成熟的国内外皮料采购渠道与品质管控体系，
            我们可为客户提供色卡选型、打样确认、小批量试单至大批量供货的全流程支持，
            帮助客户在保证触感与外观等级的前提下，优化成本、缩短上市周期。
          </p>
        </div>

        <div class="about-highlights">
          <div class="highlight-item">
            <h3>主营业务</h3>
            <ul>
              <li>✓ 耳机皮套专用革</li>
              <li>✓ 负氧离子功能革</li>
              <li>✓ 皮革贸易与配送</li>
              <li>✓ 深加工协同服务</li>
            </ul>
          </div>

          <div class="highlight-item">
            <h3>服务范围</h3>
            <ul>
              <li>✓ 色卡选型</li>
              <li>✓ 打样确认</li>
              <li>✓ 小批量试单</li>
              <li>✓ 大批量供货</li>
            </ul>
          </div>

          <div class="highlight-item">
            <h3>核心优势</h3>
            <ul>
              <li>✓ 500+色卡库存</li>
              <li>✓ 48H快速响应</li>
              <li>✓ 100+合作客户</li>
              <li>✓ RoHS环保认证</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="company-info-grid">
        <div class="info-card">
          <h3>公司规模</h3>
          <p>仓储面积3000㎡以上，配备专业检测设备和分切加工中心</p>
        </div>
        <div class="info-card">
          <h3>生产能力</h3>
          <p>分切产能日处理5000-8000平方米皮革，快速交付保障</p>
        </div>
        <div class="info-card">
          <h3>技术团队</h3>
          <p>拥有专业革料应用实验室和材料工程师，全方位技术支持</p>
        </div>
        <div class="info-card">
          <h3>品质管控</h3>
          <p>四级质控体系，色差ΔE≤要求值，追溯管理完整</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style scoped>
.about-section {
  background-color: #fff;
}

.about-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 50px;
  margin-bottom: 50px;
  align-items: start;
}

.about-text {
  color: var(--text-light);
  line-height: 2;
}

.about-text p {
  margin-bottom: 20px;
  text-align: justify;
  font-size: 1.05rem;
}

.about-highlights {
  display: grid;
  grid-template-columns: 1fr;
  gap: 25px;
}

.highlight-item {
  background: linear-gradient(135deg, #fff5f5 0%, #fff 100%);
  padding: 25px;
  border-left: 4px solid var(--primary-color);
  border-radius: 5px;
}

.highlight-item h3 {
  color: var(--primary-color);
  margin-bottom: 15px;
  font-size: 1.1rem;
}

.highlight-item ul {
  list-style: none;
}

.highlight-item li {
  color: var(--text-light);
  margin: 8px 0;
}

.company-info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 25px;
  margin-top: 40px;
}

.info-card {
  background: linear-gradient(135deg, var(--light-bg) 0%, #f9f9f9 100%);
  padding: 30px;
  border-radius: 8px;
  text-align: center;
  border-top: 4px solid var(--primary-color);
  transition: all 0.3s ease;
}

.info-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.info-card h3 {
  color: var(--primary-color);
  margin-bottom: 12px;
  font-size: 1.1rem;
}

.info-card p {
  color: var(--text-light);
  font-size: 0.95rem;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .about-content {
    grid-template-columns: 1fr;
    gap: 30px;
  }

  .about-text p {
    font-size: 1rem;
  }
}
</style>
