<template>
  <section id="contact" class="contact-section section">
    <div class="container">
      <h2 class="section-title">联系我们</h2>

      <div class="contact-content">
        <div class="contact-form">
          <h3>在线咨询</h3>
          <form @submit.prevent="handleSubmit">
            <div class="form-group">
              <label>姓名 *</label>
              <input 
                v-model="form.name" 
                type="text" 
                placeholder="请输入您的姓名" 
                required
              >
            </div>

            <div class="form-group">
              <label>公司 *</label>
              <input 
                v-model="form.company" 
                type="text" 
                placeholder="请输入您的公司名称" 
                required
              >
            </div>

            <div class="form-group">
              <label>电话 *</label>
              <input 
                v-model="form.phone" 
                type="tel" 
                placeholder="请输入您的联系电话" 
                required
              >
            </div>

            <div class="form-group">
              <label>邮箱 *</label>
              <input 
                v-model="form.email" 
                type="email" 
                placeholder="请输入您的邮箱地址" 
                required
              >
            </div>

            <div class="form-group">
              <label>产品类别 *</label>
              <select v-model="form.product" required>
                <option value="">-- 请选择 --</option>
                <option value="earphone">耳机皮套专用革</option>
                <option value="negative-ion">负氧离子功能革</option>
                <option value="trade">皮革贸易配送</option>
                <option value="processing">深加工协同</option>
                <option value="other">其他</option>
              </select>
            </div>

            <div class="form-group">
              <label>咨询内容 *</label>
              <textarea 
                v-model="form.message" 
                placeholder="请输入您的咨询内容..." 
                rows="5"
                required
              ></textarea>
            </div>

            <button type="submit" class="submit-btn">提交咨询</button>
            <p v-if="submitMessage" :class="submitStatus" class="submit-message">
              {{ submitMessage }}
            </p>
          </form>
        </div>

        <div class="contact-info">
          <h3>联系信息</h3>
          
          <div class="info-item">
            <div class="info-icon">📍</div>
            <div class="info-detail">
              <h4>公司地址</h4>
              <p>广东省东莞市</p>
              <p class="small">（详细地址请致电咨询）</p>
            </div>
          </div>

          <div class="info-item">
            <div class="info-icon">📞</div>
            <div class="info-detail">
              <h4>公司电话</h4>
              <p>18578038023</p>
              <p class="small">（周一至周五 9:00-18:00）</p>
            </div>
          </div>

          <div class="info-item">
            <div class="info-icon">📧</div>
            <div class="info-detail">
              <h4>公司邮箱</h4>
              <p><a href="mailto:1770706657@qq.com">1770706657@qq.com</a></p>
              <p class="small">（24小时回复）</p>
            </div>
          </div>

          <div class="info-item">
            <div class="info-icon">🌐</div>
            <div class="info-detail">
              <h4>官方网站</h4>
              <p><a href="http://www.yingding-leather.com" target="_blank">www.yingding-leather.com</a></p>
            </div>
          </div>

          <div class="service-hours">
            <h4>服务时间</h4>
            <ul>
              <li>❌ 周一至周五：09:00 - 18:00</li>
              <li>❌ 周六日：预约服务</li>
              <li>✅ 在线咨询：全天24小时</li>
              <li>✅ 邮件回复：24小时内</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="cta-section">
        <h3>欢迎垂询</h3>
        <p>瑛鼎拥有专业的技术团队和完善的服务体系，期待与您的合作</p>
        <div class="cta-buttons">
          <button class="cta-btn primary">立即咨询</button>
          <button class="cta-btn secondary">索要样品</button>
          <button class="cta-btn secondary">下载资料</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      form: {
        name: '',
        company: '',
        phone: '',
        email: '',
        product: '',
        message: ''
      },
      submitMessage: '',
      submitStatus: ''
    }
  },
  methods: {
    handleSubmit() {
      // 模拟提交
      if (this.form.name && this.form.company && this.form.phone && this.form.email && this.form.product && this.form.message) {
        this.submitMessage = '✓ 感谢您的咨询，我们会在24小时内回复您！'
        this.submitStatus = 'success'
        
        // 重置表单
        setTimeout(() => {
          this.form = {
            name: '',
            company: '',
            phone: '',
            email: '',
            product: '',
            message: ''
          }
          this.submitMessage = ''
        }, 3000)
      } else {
        this.submitMessage = '✗ 请填写所有必填项'
        this.submitStatus = 'error'
      }
    }
  }
}
</script>

<style scoped>
.contact-section {
  background: linear-gradient(135deg, var(--light-bg) 0%, #fff 100%);
}

.contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 50px;
  margin-bottom: 60px;
}

.contact-form h3,
.contact-info h3 {
  color: var(--primary-color);
  margin-bottom: 25px;
  font-size: 1.3rem;
}

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;
  margin-bottom: 8px;
  color: var(--text-dark);
  font-weight: 500;
}

.form-group input,
.form-group select,
.form-group textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid var(--border-color);
  border-radius: 5px;
  font-family: inherit;
  font-size: 1rem;
  color: var(--text-dark);
  transition: all 0.3s ease;
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--primary-color);
  box-shadow: 0 0 0 3px rgba(196, 30, 58, 0.1);
}

.submit-btn {
  width: 100%;
  padding: 14px;
  background: var(--primary-color);
  color: white;
  border: none;
  border-radius: 5px;
  font-weight: 600;
  font-size: 1rem;
  cursor: pointer;
  transition: all 0.3s ease;
  margin-top: 10px;
}

.submit-btn:hover {
  background: var(--accent-color);
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(196, 30, 58, 0.3);
}

.submit-message {
  margin-top: 15px;
  padding: 12px;
  border-radius: 5px;
  text-align: center;
  font-weight: 500;
}

.submit-message.success {
  background: #d4edda;
  color: #155724;
  border: 1px solid #c3e6cb;
}

.submit-message.error {
  background: #f8d7da;
  color: #721c24;
  border: 1px solid #f5c6cb;
}

.info-item {
  display: flex;
  gap: 20px;
  margin-bottom: 30px;
  padding: 20px;
  background: white;
  border-radius: 8px;
  border-left: 4px solid var(--primary-color);
}

.info-icon {
  font-size: 2rem;
  flex-shrink: 0;
}

.info-detail h4 {
  color: var(--primary-color);
  margin-bottom: 8px;
}

.info-detail p {
  color: var(--text-light);
  margin: 5px 0;
}

.info-detail p.small {
  font-size: 0.85rem;
  color: #999;
}

.service-hours {
  background: white;
  padding: 20px;
  border-radius: 8px;
  border-left: 4px solid var(--accent-color);
}

.service-hours h4 {
  color: var(--primary-color);
  margin-bottom: 15px;
}

.service-hours ul {
  list-style: none;
}

.service-hours li {
  color: var(--text-light);
  margin: 8px 0;
}

.cta-section {
  text-align: center;
  background: white;
  padding: 50px;
  border-radius: 8px;
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
}

.cta-section h3 {
  color: var(--primary-color);
  font-size: 1.8rem;
  margin-bottom: 15px;
}

.cta-section p {
  color: var(--text-light);
  margin-bottom: 30px;
  font-size: 1.05rem;
}

.cta-buttons {
  display: flex;
  gap: 20px;
  justify-content: center;
  flex-wrap: wrap;
}

.cta-btn {
  padding: 12px 30px;
  border: none;
  border-radius: 5px;
  font-weight: 600;
  font-size: 1rem;
  cursor: pointer;
  transition: all 0.3s ease;
}

.cta-btn.primary {
  background: var(--primary-color);
  color: white;
}

.cta-btn.primary:hover {
  background: var(--accent-color);
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(255, 165, 0, 0.3);
}

.cta-btn.secondary {
  background: white;
  color: var(--primary-color);
  border: 2px solid var(--primary-color);
}

.cta-btn.secondary:hover {
  background: var(--primary-color);
  color: white;
  transform: translateY(-2px);
}

@media (max-width: 768px) {
  .contact-content {
    grid-template-columns: 1fr;
    gap: 30px;
  }

  .cta-buttons {
    flex-direction: column;
  }

  .cta-btn {
    width: 100%;
  }
}
</style>
