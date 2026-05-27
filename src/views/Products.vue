<template>
  <section id="products" class="products-section section">
    <div class="container">
      <h2 class="section-title">产品体系</h2>

      <div class="products-grid">
        <div class="product-card" v-for="(product, index) in products" :key="index">
          <div class="product-icon">{{ product.icon }}</div>
          <h3>{{ product.title }}</h3>
          <p class="product-desc">{{ product.shortDesc }}</p>
          <div class="product-features">
            <span v-for="(feature, i) in product.features" :key="i" class="feature-tag">
              {{ feature }}
            </span>
          </div>
          <button class="product-btn">了解详情</button>
        </div>
      </div>

      <div class="product-details-section">
        <h3>产品亮点</h3>
        <div class="highlights-grid">
          <div class="highlight">
            <h4>耳机皮套专用革</h4>
            <ul>
              <li>蛋白皮、仿蛋白皮、超纤软革、PU纳帕等多种材质</li>
              <li>适用于耳罩、压条、头垫及收纳包</li>
              <li>支持多种纹理：荔枝纹/细纹/平纹</li>
              <li>可按客户标准定制色牢度与耐磨指标</li>
            </ul>
          </div>

          <div class="highlight">
            <h4>负氧离子功能革</h4>
            <ul>
              <li>在革层融入负氧离子释放技术</li>
              <li>兼顾装饰性与健康理念</li>
              <li>适用于耳机耳罩、座椅、汽车内饰等</li>
              <li>可提供第三方检测数据配合推广</li>
            </ul>
          </div>

          <div class="highlight">
            <h4>皮革贸易配送</h4>
            <ul>
              <li>代理国内外优质牛皮、羊皮、PU/PVC革</li>
              <li>支持整卷、裁片、按色卡订货</li>
              <li>东莞本地仓储，珠三角当日达</li>
              <li>省外物流专线配送，24-72小时送达</li>
            </ul>
          </div>

          <div class="highlight">
            <h4>深加工协同</h4>
            <ul>
              <li>合作裁切、冲孔、丝印服务</li>
              <li>热压logo、激光雕花等后工序</li>
              <li>从皮料采购到裁片成品一站式完成</li>
              <li>公差可控，质量稳定</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="applications-section">
        <h3>应用领域</h3>
        <div class="industries-grid">
          <div class="industry-item" v-for="industry in industries" :key="industry">
            {{ industry }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Products',
  data() {
    return {
      products: [
        {
          title: '耳机皮套专用革',
          icon: '🎧',
          shortDesc: '专为耳机设计的包覆革料，强调亲肤柔软、耐汗耐腐蚀',
          features: ['蛋白皮', '超纤软革', 'PU纳帕', '可定制']
        },
        {
          title: '负氧离子功能革',
          icon: '✨',
          shortDesc: '融入负氧离子释放技术的健康革料',
          features: ['健康功能', '持续释放', '可检测', '多场景']
        },
        {
          title: '皮革贸易配送',
          icon: '📦',
          shortDesc: '代理国内外优质皮革，快速配送服务',
          features: ['品种齐全', '价格优势', '快速配送', '灵活结算']
        },
        {
          title: '深加工协同',
          icon: '⚙️',
          shortDesc: '完整的后工序加工支持服务',
          features: ['裁切加工', '丝印烫印', '复合服务', '一站式']
        }
      ],
      industries: [
        '耳机音频', '智能穿戴', '汽车内饰', '家具软装',
        '箱包皮具', '养生健康', '电竞外设', '礼品定制'
      ]
    }
  }
}
</script>

<style scoped>
.products-section {
  background-color: #fff;
}

.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 25px;
  margin-bottom: 60px;
}

.product-card {
  background: linear-gradient(135deg, #fff 0%, var(--light-bg) 100%);
  padding: 30px;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  text-align: center;
  border-top: 4px solid var(--primary-color);
}

.product-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
}

.product-icon {
  font-size: 3rem;
  margin-bottom: 15px;
}

.product-card h3 {
  color: var(--primary-color);
  margin-bottom: 12px;
  font-size: 1.1rem;
}

.product-desc {
  color: var(--text-light);
  margin-bottom: 15px;
  line-height: 1.6;
  font-size: 0.95rem;
}

.product-features {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  justify-content: center;
  margin-bottom: 20px;
}

.feature-tag {
  background: var(--primary-color);
  color: white;
  padding: 5px 12px;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 500;
}

.product-btn {
  background: var(--primary-color);
  color: white;
  padding: 10px 25px;
  border: none;
  border-radius: 5px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  width: 100%;
}

.product-btn:hover {
  background: var(--accent-color);
  transform: scale(1.02);
}

.product-details-section {
  margin-bottom: 60px;
}

.product-details-section h3 {
  font-size: 1.8rem;
  color: var(--primary-color);
  text-align: center;
  margin-bottom: 40px;
}

.highlights-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 25px;
}

.highlight {
  background: var(--light-bg);
  padding: 25px;
  border-radius: 8px;
  border-left: 4px solid var(--primary-color);
}

.highlight h4 {
  color: var(--primary-color);
  margin-bottom: 15px;
  font-size: 1rem;
}

.highlight ul {
  list-style: none;
}

.highlight li {
  color: var(--text-light);
  margin: 10px 0;
  padding-left: 20px;
  position: relative;
  font-size: 0.95rem;
}

.highlight li:before {
  content: '✓';
  position: absolute;
  left: 0;
  color: var(--accent-color);
  font-weight: bold;
}

.applications-section {
  background: var(--light-bg);
  padding: 40px;
  border-radius: 8px;
}

.applications-section h3 {
  font-size: 1.5rem;
  color: var(--primary-color);
  text-align: center;
  margin-bottom: 30px;
}

.industries-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  gap: 15px;
}

.industry-item {
  background: white;
  padding: 15px;
  text-align: center;
  border-radius: 5px;
  color: var(--text-dark);
  font-weight: 500;
  border: 1px solid var(--border-color);
  transition: all 0.3s ease;
}

.industry-item:hover {
  background: var(--primary-color);
  color: white;
  border-color: var(--primary-color);
}

@media (max-width: 768px) {
  .products-grid {
    grid-template-columns: 1fr;
  }

  .highlights-grid {
    grid-template-columns: 1fr;
  }

  .industries-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>
