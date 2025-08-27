# 🏠 房间房租分配系统 / Room Rent Allocation System

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-blue)](https://your-username.github.io/your-repo-name)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/Version-2.2.2-green.svg)](https://github.com/your-username/your-repo-name/releases)

[中文](#中文文档) | [English](#english-documentation)

---

## 中文文档

### 📖 项目简介

房间房租分配系统是一个基于**调整获胜者算法**的公平分配工具，帮助合租人员根据个人偏好和经济能力公平分配房间和房租。

🌟 **在线体验**: [GitHub Pages 演示](https://your-username.github.io/your-repo-name)

### ✨ 主要特性

#### 🎯 核心功能
- **智能分配算法**: 基于Shapley值的调整获胜者算法
- **公平性保证**: 多维度公平性分析和满意度评估
- **动态参与者**: 支持任意数量的房间和人员
- **透明化过程**: 详细的分配过程和计算解释
- **多房间折扣**: 自动计算多房间租赁的优惠

#### 🌍 用户体验
- **双语支持**: 完整的中英文国际化
- **现代化UI**: Microsoft Fluent UI设计系统
- **响应式设计**: 支持桌面、平板、手机
- **专业报告**: 一键导出PDF分配报告
- **实时计算**: 即时显示分配结果和公平性指标

#### 📊 可视化功能
- **交互式图表**: Chart.js驱动的动态图表
- **公平性仪表盘**: 直观的满意度进度条
- **详细解释**: 算法步骤和决策依据展示

### 🚀 快速开始

#### 在线使用 (推荐)
1. 访问 [在线演示](https://your-username.github.io/your-repo-name)
2. 设置总房租和参与人员
3. 为每个房间输入出价
4. 点击"计算公平分配"
5. 查看结果并导出PDF报告

#### 本地部署 (Web版本)
```bash
# 克隆项目
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

# 使用任意HTTP服务器
python -m http.server 8000
# 或
npx serve .

# 访问 http://localhost:8000/web-index.html
```

#### 桌面应用 (Electron版本)
```bash
# 安装依赖
npm install

# 启动应用
npm start

# 构建桌面应用
npm run build
```

### 📋 使用说明

#### 1. 基本设置
- **总房租**: 输入需要分摊的总租金（支持镑/周或自定义单位）
- **人员管理**: 添加/删除参与分配的人员

#### 2. 房间出价
- **添加房间**: 根据实际情况添加房间（A、B、C...）
- **设置出价**: 每个人为每个房间输入心理价位
- **出价策略**: 出价应反映个人对房间的真实偏好

#### 3. 分配计算
- **算法执行**: 系统运行调整获胜者算法
- **结果展示**: 显示房间分配和最终房租
- **公平性分析**: 查看满意度指标和公平性评分

#### 4. 结果导出
- **PDF报告**: 包含完整分配信息的专业报告
- **多语言**: 报告内容支持中英文

### 🧮 算法原理

#### 调整获胜者算法 (Adjusted Winner Algorithm)
本系统采用基于博弈论的公平分配算法，确保：

1. **比例公平性**: 根据个人出价比例分配资源
2. **帕累托最优**: 在不损害他人利益的前提下最大化整体满意度
3. **激励相容**: 鼓励参与者诚实报价

#### 三阶段分配流程
```
阶段1: 初始分配
├── 计算出价比例
├── 识别最优匹配
└── 分配核心房间

阶段2: 房租计算  
├── 基础房租计算
├── 多房间折扣应用
└── 预算平衡调整

阶段3: 公平性优化
├── 满意度评估
├── 公平性指标
└── 最终结果验证
```

### 📊 应用场景

#### 🏠 生活场景
- **学生合租**: 大学生宿舍和校外租房
- **白领合租**: 城市青年共享居住空间
- **家庭分房**: 多代同堂的房间安排
- **短期租赁**: 出差、旅游的临时住宿

#### 💼 商业场景
- **企业宿舍**: 员工住宿安排和成本分摊
- **联合办公**: 工位和会议室的公平分配
- **酒店管理**: 团体客户的房间分配优化
- **房产中介**: 租赁方案的专业咨询工具

### 🛠️ 技术栈

#### 前端技术
- **框架**: Vanilla JavaScript (ES6+)
- **UI库**: Microsoft Fluent UI Web Components
- **图表**: Chart.js
- **样式**: CSS3 + CSS Grid + Flexbox
- **国际化**: 自研i18n系统

#### 后端/计算
- **算法**: JavaScript实现的博弈论算法
- **数据处理**: 纯前端计算，无服务器依赖
- **PDF生成**: jsPDF + html2canvas

#### 部署平台
- **Web版本**: GitHub Pages (静态托管)
- **桌面版本**: Electron (跨平台)
- **CI/CD**: GitHub Actions自动部署

### 📱 兼容性

#### 浏览器支持
- Chrome 85+ ✅
- Firefox 80+ ✅  
- Safari 14+ ✅
- Edge 85+ ✅

#### 操作系统
- Windows 10/11 ✅
- macOS 10.14+ ✅
- Ubuntu 18.04+ ✅
- iOS Safari ✅
- Android Chrome ✅

### 🤝 贡献指南

我们欢迎社区贡献！请查看 [贡献指南](CONTRIBUTING.md) 了解详情。

#### 开发环境设置
```bash
# Fork 项目
git clone https://github.com/your-username/your-repo-name.git

# 创建功能分支
git checkout -b feature/amazing-feature

# 提交更改
git commit -m 'Add some amazing feature'

# 推送分支
git push origin feature/amazing-feature

# 创建 Pull Request
```

### 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

### 📞 联系我们

- **问题反馈**: [GitHub Issues](https://github.com/your-username/your-repo-name/issues)
- **功能建议**: [GitHub Discussions](https://github.com/your-username/your-repo-name/discussions)
- **邮件联系**: your-email@example.com

---

## English Documentation

### 📖 Project Overview

The Room Rent Allocation System is a fair allocation tool based on the **Adjusted Winner Algorithm**, helping roommates fairly distribute rooms and rent according to personal preferences and financial capabilities.

🌟 **Live Demo**: [GitHub Pages Demo](https://your-username.github.io/your-repo-name)

### ✨ Key Features

#### 🎯 Core Functions
- **Smart Allocation Algorithm**: Adjusted Winner Algorithm based on Shapley values
- **Fairness Guarantee**: Multi-dimensional fairness analysis and satisfaction assessment
- **Dynamic Participants**: Support for any number of rooms and people
- **Transparent Process**: Detailed allocation process and calculation explanations
- **Multi-room Discount**: Automatic calculation of multi-room rental discounts

#### 🌍 User Experience
- **Bilingual Support**: Complete Chinese-English internationalization
- **Modern UI**: Microsoft Fluent UI design system
- **Responsive Design**: Support for desktop, tablet, and mobile
- **Professional Reports**: One-click PDF allocation report export
- **Real-time Calculation**: Instant display of allocation results and fairness indicators

#### 📊 Visualization Features
- **Interactive Charts**: Dynamic charts powered by Chart.js
- **Fairness Dashboard**: Intuitive satisfaction progress bars
- **Detailed Explanations**: Algorithm steps and decision rationale display

### 🚀 Quick Start

#### Online Usage (Recommended)
1. Visit [Live Demo](https://your-username.github.io/your-repo-name)
2. Set total rent and participants
3. Enter bids for each room
4. Click "Calculate Fair Allocation"
5. View results and export PDF report

#### Local Deployment (Web Version)
```bash
# Clone the project
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

# Use any HTTP server
python -m http.server 8000
# or
npx serve .

# Visit http://localhost:8000/web-index.html
```

#### Desktop Application (Electron Version)
```bash
# Install dependencies
npm install

# Start application
npm start

# Build desktop app
npm run build
```

### 📋 Usage Instructions

#### 1. Basic Setup
- **Total Rent**: Enter the total rent to be shared (supports £/week or custom units)
- **People Management**: Add/remove participants in the allocation

#### 2. Room Bidding
- **Add Rooms**: Add rooms according to actual situation (A, B, C...)
- **Set Bids**: Each person enters their psychological price for each room
- **Bidding Strategy**: Bids should reflect personal true preferences for rooms

#### 3. Allocation Calculation
- **Algorithm Execution**: System runs the Adjusted Winner Algorithm
- **Results Display**: Shows room allocation and final rent
- **Fairness Analysis**: View satisfaction metrics and fairness scores

#### 4. Results Export
- **PDF Report**: Professional report with complete allocation information
- **Multilingual**: Report content supports Chinese and English

### 🧮 Algorithm Principles

#### Adjusted Winner Algorithm
This system uses a game theory-based fair allocation algorithm that ensures:

1. **Proportional Fairness**: Allocate resources based on individual bid ratios
2. **Pareto Optimality**: Maximize overall satisfaction without harming others' interests
3. **Incentive Compatibility**: Encourage participants to bid honestly

#### Three-Stage Allocation Process
```
Stage 1: Initial Allocation
├── Calculate bid ratios
├── Identify optimal matches
└── Allocate core rooms

Stage 2: Rent Calculation
├── Base rent calculation
├── Multi-room discount application
└── Budget balance adjustment

Stage 3: Fairness Optimization
├── Satisfaction assessment
├── Fairness indicators
└── Final result verification
```

### 📊 Use Cases

#### 🏠 Living Scenarios
- **Student Housing**: University dorms and off-campus rentals
- **Professional Sharing**: Urban young professionals sharing living spaces
- **Family Room Assignment**: Multi-generational household room arrangements
- **Short-term Rentals**: Temporary accommodation for business trips and travel

#### 💼 Business Scenarios
- **Corporate Housing**: Employee accommodation arrangements and cost sharing
- **Co-working Spaces**: Fair allocation of workstations and meeting rooms
- **Hotel Management**: Room allocation optimization for group customers
- **Real Estate**: Professional consulting tool for rental solutions

### 🛠️ Tech Stack

#### Frontend Technologies
- **Framework**: Vanilla JavaScript (ES6+)
- **UI Library**: Microsoft Fluent UI Web Components
- **Charts**: Chart.js
- **Styling**: CSS3 + CSS Grid + Flexbox
- **Internationalization**: Custom i18n system

#### Backend/Computation
- **Algorithm**: JavaScript implementation of game theory algorithms
- **Data Processing**: Pure frontend computation, no server dependencies
- **PDF Generation**: jsPDF + html2canvas

#### Deployment Platforms
- **Web Version**: GitHub Pages (static hosting)
- **Desktop Version**: Electron (cross-platform)
- **CI/CD**: GitHub Actions automated deployment

### 📱 Compatibility

#### Browser Support
- Chrome 85+ ✅
- Firefox 80+ ✅
- Safari 14+ ✅
- Edge 85+ ✅

#### Operating Systems
- Windows 10/11 ✅
- macOS 10.14+ ✅
- Ubuntu 18.04+ ✅
- iOS Safari ✅
- Android Chrome ✅

### 🤝 Contributing

We welcome community contributions! Please see [Contributing Guide](CONTRIBUTING.md) for details.

#### Development Environment Setup
```bash
# Fork the project
git clone https://github.com/your-username/your-repo-name.git

# Create feature branch
git checkout -b feature/amazing-feature

# Commit changes
git commit -m 'Add some amazing feature'

# Push branch
git push origin feature/amazing-feature

# Create Pull Request
```

### 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### 📞 Contact Us

- **Issue Reports**: [GitHub Issues](https://github.com/your-username/your-repo-name/issues)
- **Feature Requests**: [GitHub Discussions](https://github.com/your-username/your-repo-name/discussions)
- **Email Contact**: your-email@example.com

---

## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=your-username/your-repo-name&type=Date)](https://star-history.com/#your-username/your-repo-name&Date)

## 📈 Statistics

![GitHub stars](https://img.shields.io/github/stars/your-username/your-repo-name?style=social)
![GitHub forks](https://img.shields.io/github/forks/your-username/your-repo-name?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/your-username/your-repo-name?style=social)

---

**🎉 感谢使用房间房租分配系统！ / Thank you for using the Room Rent Allocation System!** ✨