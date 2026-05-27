<template>
  <section id="advantages" class="advantages-section section">
    <div class="container">
      <h2 class="section-title">核心优势</h2>

      <div class="advantages-grid">
        <div class="advantage-card">
          <div class="card-icon">⚙️</div>
          <h3>技术创新</h3>
          <p>配备专业革料应用实验室，可模拟贴合工艺进行验证，从厚度、含油率、剥离强度等维度提供专业建议</p>
        </div>

        <div class="advantage-card">
          <div class="card-icon">📦</div>
          <h3>物流快捷</h3>
          <p>与顺丰、德邦合作，珠三角上午下单下午发货，省外48-72小时送达，支持月结账期</p>
        </div>

        <div class="advantage-card">
          <div class="card-icon">🎨</div>
          <h3>色卡丰富</h3>
          <p>常备500+色卡与现货SKU，支持Pantone色号定制，3-5个工作日快速打样</p>
        </div>

        <div class="advantage-card">
          <div class="card-icon">✅</div>
          <h3>品质认证</h3>
          <p>合作皮厂通过ISO9001认证，支持REACH、RoHS、SGS检测报告，可提供追溯管理</p>
        </div>

        <div class="advantage-card">
          <div class="card-icon">🔧</div>
          <h3>深加工支持</h3>
          <p>配备大型裁床与自动裁切线，支持裁片、丝印、烫印、复合等后工序一站式服务</p>
        </div>

        <div class="advantage-card">
          <div class="card-icon">🌟</div>
          <h3>功能革创新</h3>
          <p>负氧离子革配方由合作实验室持续迭代，可提供功能检测数据支撑产品推广</p>
        </div>
      </div>

      <div class="advantages-detailed">
        <div class="detailed-section">
          <h3>品质管控四级体系</h3>
          <div class="process-flow">
            <div class="flow-step">
              <div class="step-number">1</div>
              <p>供应商准入</p>
            </div>
            <div class="flow-arrow">→</div>
            <div class="flow-step">
              <div class="step-number">2</div>
              <p>来料检验</p>
            </div>
            <div class="flow-arrow">→</div>
            <div class="flow-step">
              <div class="step-number">3</div>
              <p>仓储养护</p>
            </div>
            <div class="flow-arrow">→</div>
            <div class="flow-step">
              <div class="step-number">4</div>
              <p>出库复核</p>
            </div>
          </div>
        </div>

        <div class="detailed-section">
          <h3>服务流程完整</h3>
          <div class="service-list">
            <div class="service-item">
              <span class="item-number">01</span>
              <span class="item-text">需求沟通</span>
            </div>
            <div class="service-item">
              <span class="item-number">02</span>
              <span class="item-text">色卡选型</span>
            </div>
            <div class="service-item">
              <span class="item-number">03</span>
              <span class="item-text">打样确认</span>
            </div>
            <div class="service-item">
              <span class="item-number">04</span>
              <span class="item-text">合同签订</span>
            </div>
            <div class="service-item">
              <span class="item-number">05</span>
              <span class="item-text">备货分切</span>
            </div>
            <div class="service-item">
              <span class="item-number">06</span>
              <span class="item-text">质检出库</span>
            </div>
            <div class="service-item">
              <span class="item-number">07</span>
              <span class="item-text">物流配送</span>
            </div>
            <div class="service-item">
              <span class="item-number">08</span>
              <span class="item-text">贴合指导</span>
            </div>
            <div class="service-item">
              <span class="item-number">09</span>
              <span class="item-text">售后跟踪</span>
            </div>
            <div class="service-item">
              <span class="item-number">10</span>
              <span class="item-text">复购优化</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Advantages'
}
</script>

<style scoped>
.advantages-section {
  background-color: var(--light-bg);
}

.advantages-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 25px;
  margin-bottom: 60px;
}

.advantage-card {
  background: white;
  padding: 30px;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  text-align: center;
}

.advantage-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
}

.card-icon {
  font-size: 2.5rem;
  margin-bottom: 15px;
}

.advantage-card h3 {
  color: var(--primary-color);
  margin-bottom: 15px;
  font-size: 1.1rem;
}

.advantage-card p {
  color: var(--text-light);
  line-height: 1.7;
  font-size: 0.95rem;
}

.advantages-detailed {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  gap: 40px;
  margin-top: 50px;
}

.detailed-section h3 {
  color: var(--primary-color);
  margin-bottom: 25px;
  font-size: 1.2rem;
  text-align: center;
}

.process-flow {
  display: flex;
  justify-content: space-around;
  align-items: center;
  background: white;
  padding: 30px;
  border-radius: 8px;
  flex-wrap: wrap;
  gap: 10px;
}

.flow-step {
  flex: 0 0 auto;
  text-align: center;
}

.step-number {
  width: 50px;
  height: 50px;
  background: linear-gradient(135deg, var(--primary-color), #a01530);
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  font-size: 1.2rem;
  margin: 0 auto 10px;
}

.flow-step p {
  color: var(--text-light);
  font-size: 0.9rem;
  font-weight: 500;
}

.flow-arrow {
  color: var(--primary-color);
  font-size: 1.5rem;
  font-weight: bold;
}

.service-list {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  background: white;
  padding: 30px;
  border-radius: 8px;
}

.service-item {
  display: flex;
  align-items: center;
  gap: 15px;
}

.item-number {
  width: 45px;
  height: 45px;
  background: var(--accent-color);
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  flex-shrink: 0;
}

.item-text {
  color: var(--text-dark);
  font-weight: 500;
}

@media (max-width: 768px) {
  .advantages-grid {
    grid-template-columns: 1fr;
  }

  .advantages-detailed {
    grid-template-columns: 1fr;
  }

  .process-flow {
    flex-direction: column;
    gap: 20px;
  }

  .flow-arrow {
    transform: rotate(90deg);
  }

  .service-list {
    grid-template-columns: 1fr;
  }
}
</style>
