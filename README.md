# 瑛鼎塑胶制品公司官方网站

东莞市瑛鼎塑胶制品有限公司的专业网站，展示公司产品、服务和联系方式。

## 项目信息

- **公司名称**：东莞市瑛鼎塑胶制品有限公司
- **英文名称**：Dongguan Yingding Plastic & Leather Trading Co., Ltd.
- **主要产品**：耳机皮套、负氧离子革、皮革贸易
- **网址**：www.yingding-leather.com

## 技术栈

- **框架**：Vue 3
- **构建工具**：Vite
- **样式**：CSS3 + Responsive Design
- **部署**：支持静态文件部署

## 项目结构

```
yingding-website/
├── index.html              # HTML入口文件
├── package.json            # 项目配置
├── vite.config.js          # Vite配置
└── src/
    ├── main.js             # 应用入口
    ├── App.vue             # 根组件
    ├── assets/
    │   └── styles.css      # 全局样式
    ├── components/
    │   ├── Header.vue      # 页头组件
    │   └── Footer.vue      # 页脚组件
    └── views/
        ├── Home.vue        # 首页
        ├── About.vue       # 公司简介
        ├── Advantages.vue  # 核心优势
        ├── Products.vue    # 产品体系
        └── Contact.vue     # 联系我们
```

## 安装与运行

### 1. 安装依赖

```bash
npm install
```

### 2. 开发模式

```bash
npm run dev
```

浏览器会自动打开 `http://localhost:5173`

### 3. 生产构建

```bash
npm run build
```

生成 `dist` 文件夹，包含可部署的静态文件。

### 4. 预览生产构建

```bash
npm run preview
```

## 功能特性

### 首页（Home）
- 英雄区域展示
- 核心指标统计
- 核心优势展示

### 公司简介（About）
- 公司背景介绍
- 主营业务详情
- 公司规模展示

### 核心优势（Advantages）
- 六大竞争优势
- 品质管控体系
- 完整服务流程

### 产品体系（Products）
- 四大产品线展示
- 产品详细特性
- 应用领域介绍

### 联系我们（Contact）
- 在线咨询表单
- 联系信息展示
- 服务时间说明

## 响应式设计

网站完全响应式，支持：
- 📱 手机（< 768px）
- 📱 平板（768px - 1024px）
- 🖥️ 桌面（> 1024px）

## 颜色方案

- **主色**：#C41E3A（瑛红）
- **辅色**：#333333（深灰）
- **强调色**：#FFA500（橙色）
- **浅色背景**：#F5F5F5

## 联系方式

- **电话**：0769-XXXX XXXX
- **邮箱**：sales@yingding.com
- **网址**：www.yingding-leather.com
- **地址**：广东省东莞市

## 部署建议

### GitHub Pages 部署
```bash
npm run build
# 将 dist 文件夹上传到 GitHub Pages
```

### 其他静态主机
- Netlify
- Vercel
- 阿里云 OSS
- 腾讯云 COS

## 功能扩展

可以扩展的功能：
- [ ] 动态数据后端服务
- [ ] 邮件通知功能
- [ ] 产品搜索和筛选
- [ ] 在线商城功能
- [ ] 新闻博客模块
- [ ] 多语言支持
- [ ] SEO优化
- [ ] 分析统计

## 许可证

© 2024 东莞市瑛鼎塑胶制品有限公司。版权所有。

## 维护说明

- 更新公司信息时，修改 `src/components/Header.vue` 中的联系方式
- 修改配色方案时，更新 `src/assets/styles.css` 中的 CSS 变量
- 新增产品时，修改 `src/views/Products.vue` 中的产品数据
- 更新内容时，直接编辑对应的 Vue 文件

---

**网站开发完成日期**：2024年
**最后更新**：2024年
