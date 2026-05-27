<template>
  <section id="home" class="home-section">
    <div class="hero">
      <div class="container">
        <div class="hero-content">
          <h2>欢迎来到瑛鼎塑胶</h2>
          <p class="hero-subtitle">专业皮革贸易与功能革解决方案供应商</p>
          <p class="hero-description">
            为全球耳机品牌、ODM工厂及皮具加工厂提供优质皮革材料、专业选皮与快速交付服务
          </p>
          <div class="hero-cta">
            <button class="btn btn-primary">了解更多</button>
            <button class="btn btn-secondary">在线咨询</button>
          </div>
        </div>
      </div>
    </div>

    <div class="container stats-section">
      <h3 class="section-subtitle">核心指标</h3>
      <div class="stats-grid">
        <div class="stat-card" v-for="stat in stats" :key="stat.label">
          <div class="stat-number">{{ stat.number }}</div>
          <div class="stat-label">{{ stat.label }}</div>
        </div>
      </div>
    </div>

    <div class="features-section">
      <div class="container">
        <h3 class="section-subtitle">为什么选择瑛鼎</h3>
        <div class="features-grid">
          <div class="feature-item">
            <div class="feature-icon">⚡</div>
            <h4>快速响应</h4>
            <p>48小时常规样品响应，珠三角当日达</p>
          </div>
          <div class="feature-item">
            <div class="feature-icon">🎨</div>
            <h4>色卡丰富</h4>
            <p>500+常备色卡与现货SKU，专业选皮团队</p>
          </div>
          <div class="feature-item">
            <div class="feature-icon">✅</div>
            <h4>品质保证</h4>
            <p>四级质控体系，RoHS环保合规</p>
          </div>
          <div class="feature-item">
            <div class="feature-icon">🌍</div>
            <h4>全球服务</h4>
            <p>100+合作客户，国内外订单均可处理</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      stats: [
        { number: '500+', label: '常备色卡SKU' },
        { number: '48H', label: '样品响应' },
        { number: '100+', label: '合作客户' },
        { number: '10+', label: '皮革品类' }
      ]
    }
  }
}
</script>

<style scoped>
.home-section {
  flex: 1;
}

.hero {
  background: linear-gradient(135deg, var(--primary-color) 0%, #a01530 100%);
  color: white;
  padding: 80px 20px;
  text-align: center;
}

.hero-content h2 {
  font-size: 2.8rem;
  margin-bottom: 20px;
  font-weight: bold;
}

.hero-subtitle {
  font-size: 1.3rem;
  margin-bottom: 15px;
  opacity: 0.95;
}

.hero-description {
  font-size: 1.05rem;
  max-width: 600px;
  margin: 0 auto 30px;
  line-height: 1.8;
  opacity: 0.9;
}

.hero-cta {
  display: flex;
  gap: 20px;
  justify-content: center;
  flex-wrap: wrap;
}

.btn {
  padding: 12px 35px;
  font-size: 1rem;
  border: none;
  border-radius: 5px;
  font-weight: 600;
  transition: all 0.3s ease;
}

.btn-primary {
  background-color: var(--accent-color);
  color: #fff;
}

.btn-primary:hover {
  background-color: #ff8c00;
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(255, 165, 0, 0.3);
}

.btn-secondary {
  background-color: transparent;
  color: white;
  border: 2px solid white;
}

.btn-secondary:hover {
  background-color: rgba(255, 255, 255, 0.1);
  transform: translateY(-2px);
}

.stats-section {
  padding: 60px 20px;
  background-color: var(--light-bg);
}

.section-subtitle {
  font-size: 1.8rem;
  font-weight: bold;
  color: var(--primary-color);
  text-align: center;
  margin-bottom: 40px;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 30px;
}

.stat-card {
  background: white;
  padding: 30px;
  border-radius: 8px;
  text-align: center;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
}

.stat-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.15);
}

.stat-number {
  font-size: 2.5rem;
  font-weight: bold;
  color: var(--primary-color);
  margin-bottom: 10px;
}

.stat-label {
  color: var(--text-light);
  font-weight: 500;
}

.features-section {
  padding: 60px 20px;
  background-color: #fff;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 30px;
}

.feature-item {
  text-align: center;
  padding: 30px;
  border-radius: 8px;
  background-color: var(--light-bg);
  transition: all 0.3s ease;
}

.feature-item:hover {
  background-color: #f0f0f0;
  transform: translateY(-5px);
}

.feature-icon {
  font-size: 2.5rem;
  margin-bottom: 15px;
}

.feature-item h4 {
  font-size: 1.2rem;
  margin-bottom: 10px;
  color: var(--primary-color);
}

.feature-item p {
  color: var(--text-light);
  line-height: 1.6;
}

@media (max-width: 768px) {
  .hero-content h2 {
    font-size: 2rem;
  }
  
  .hero-subtitle {
    font-size: 1.1rem;
  }
  
  .hero-cta {
    flex-direction: column;
    align-items: center;
  }
  
  .btn {
    width: 100%;
    max-width: 300px;
  }
}
</style>
