# 🏠 房间房租分配系统 / Room Rent Allocation System

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-blue)](#在线演示)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/Version-2.2.2-green.svg)](#版本历史)
[![Language](https://img.shields.io/badge/Language-JavaScript-yellow.svg)](https://github.com/topics/javascript)
[![Framework](https://img.shields.io/badge/UI-Fluent%20UI-blue.svg)](https://github.com/microsoft/fluentui)

[中文](#中文文档) | [English](#english-documentation)

> 🎯 基于博弈论的智能房间分配系统，让合租变得更公平！  
> 🌍 Smart room allocation system based on game theory for fair roommate arrangements!

---

## 中文文档

### 📖 项目简介

房间房租分配系统是一个基于**调整获胜者算法**的公平分配工具，帮助合租人员根据个人偏好和经济能力公平分配房间和房租。

🌟 **在线体验**: 访问 `http://localhost:8080/web-index.html` 查看本地演示  
📱 **移动端**: 完美支持手机和平板设备  
⚡ **即开即用**: 无需安装，打开浏览器即可使用

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
1. 启动本地服务器: `python -m http.server 8080`
2. 访问 `http://localhost:8080/web-index.html`
3. 设置总房租和参与人员
4. 为每个房间输入出价
5. 点击"计算公平分配"
6. 查看结果并导出PDF报告

#### GitHub Pages部署
1. Fork 此项目到您的GitHub账户
2. 启用 GitHub Pages (Settings -> Pages -> GitHub Actions)
3. 访问 `https://your-username.github.io/repository-name`

#### 本地开发 (Web版本)
```bash
# 下载项目文件
# 将所有文件放在同一目录下

# 使用Python启动服务器
python -m http.server 8080

# 或使用Node.js
npx serve . -p 8080

# 访问 http://localhost:8080/web-index.html
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

#### 🎮 使用示例
```
场景: 三人合租，总房租 £300/周

人员: 张三、李四、王五
房间: A房间(朝南大房)、B房间(朝北中房)、C房间(朝西小房)

出价矩阵:
        A房间   B房间   C房间
张三     120     90     60
李四     100    100     70
王五      80     80     80

算法结果:
张三 → A房间 (£110/周)
李四 → B房间 (£95/周)  
王五 → C房间 (£95/周)

公平性: 各人满意度均超过85%
```

#### 1. 基本设置
- **总房租**: 输入需要分摊的总租金（支持镑/周或自定义单位）
- **人员管理**: 点击"+ 添加人员"按钮动态增加参与者
- **语言切换**: 右上角可切换中英文界面

#### 2. 房间出价
- **添加房间**: 点击"+ 添加房间"按钮添加房间（A、B、C...）
- **设置出价**: 每个人为每个房间输入心理价位
- **出价策略**: 建议出价反映真实偏好，有利于获得更满意的分配

#### 3. 分配计算
- **一键计算**: 点击"计算公平分配"运行算法
- **结果展示**: 实时显示房间分配和最终房租
- **公平性分析**: 查看每个人的满意度和整体公平性指数
- **详细解释**: 了解算法的每一步决策过程

#### 4. 结果导出
- **PDF报告**: 生成包含完整分配信息的专业报告
- **多语言**: 报告内容自动匹配当前界面语言
- **分享便利**: 可直接分享给所有参与者

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

🌟 **Live Demo**: Visit `http://localhost:8080/web-index.html` for local demo  
📱 **Mobile Ready**: Perfect support for phones and tablets  
⚡ **Instant Use**: No installation required, just open in browser

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
1. Start local server: `python -m http.server 8080`
2. Visit `http://localhost:8080/web-index.html`
3. Set total rent and participants
4. Enter bids for each room
5. Click "Calculate Fair Allocation"
6. View results and export PDF report

#### GitHub Pages Deployment
1. Fork this project to your GitHub account
2. Enable GitHub Pages (Settings -> Pages -> GitHub Actions)
3. Visit `https://your-username.github.io/repository-name`

#### Local Development (Web Version)
```bash
# Download project files
# Place all files in the same directory

# Use Python to start server
python -m http.server 8080

# Or use Node.js
npx serve . -p 8080

# Visit http://localhost:8080/web-index.html
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

#### 🎮 Usage Example
```
Scenario: 3 roommates, total rent £300/week

People: Alice, Bob, Charlie
Rooms: Room A(South-facing large), Room B(North-facing medium), Room C(West-facing small)

Bid Matrix:
         Room A  Room B  Room C
Alice      120      90      60
Bob        100     100      70
Charlie     80      80      80

Algorithm Result:
Alice → Room A (£110/week)
Bob → Room B (£95/week)
Charlie → Room C (£95/week)

Fairness: All satisfaction rates above 85%
```

#### 1. Basic Setup
- **Total Rent**: Enter the total rent to be shared (supports £/week or custom units)
- **People Management**: Click "+ Add Person" to dynamically add participants
- **Language Switch**: Toggle between Chinese and English in the top-right corner

#### 2. Room Bidding
- **Add Rooms**: Click "+ Add Room" to add rooms (A, B, C...)
- **Set Bids**: Each person enters their psychological price for each room
- **Bidding Strategy**: Honest bidding recommended for optimal satisfaction

#### 3. Allocation Calculation
- **One-Click Calculate**: Click "Calculate Fair Allocation" to run algorithm
- **Results Display**: Real-time display of room allocation and final rent
- **Fairness Analysis**: View individual satisfaction and overall fairness index
- **Detailed Explanation**: Understand each step of the algorithm's decision process

#### 4. Results Export
- **PDF Report**: Generate professional report with complete allocation information
- **Multilingual**: Report content automatically matches current interface language
- **Easy Sharing**: Can be directly shared with all participants

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

## 🎯 项目特色 / Project Highlights

### 🔬 技术创新
- **纯前端算法**: 无服务器依赖，完全在浏览器中运行
- **博弈论应用**: 真正的学术级算法实现
- **响应式设计**: 一套代码适配所有设备

### 🎨 用户体验
- **零学习成本**: 直观的操作界面，老少皆宜
- **实时反馈**: 输入即时验证，结果立即显示
- **专业报告**: 银行级PDF生成质量

### 🌍 开放生态
- **完全开源**: MIT许可证，自由使用和修改
- **社区驱动**: 欢迎贡献代码和想法
- **多平台部署**: 支持Web、桌面、移动端

## 🚀 版本历史 / Version History

| 版本 | 日期 | 主要更新 |
|------|------|----------|
| v2.2.2 | 2025-08 | 🔄 恢复滚动布局，优化用户体验 |
| v2.2.1 | 2025-08 | 🎨 简约白蓝配色，修复PDF导出 |
| v2.2.0 | 2025-08 | 🌍 Fluent UI集成，完整国际化 |
| v2.1.0 | 2025-08 | 📊 动态房间人员，公平性分析 |
| v2.0.0 | 2025-08 | 🧮 调整获胜者算法重构 |
| v1.0.0 | 2025-08 | 🎉 基础功能发布 |

## 🤝 贡献者 / Contributors

感谢所有为这个项目做出贡献的开发者！  
Thanks to all the developers who contributed to this project!

## 📊 使用统计 / Usage Statistics

- 🏠 **适用场景**: 学生宿舍、白领合租、家庭分房、企业住宿
- 🌍 **支持语言**: 中文、English (更多语言开发中)
- 📱 **兼容平台**: Windows、macOS、Linux、iOS、Android
- ⚡ **响应速度**: 平均计算时间 < 100ms

## 🔗 相关链接 / Related Links

- 📖 [部署指南 / Deployment Guide](./DEPLOYMENT.md)
- 🐛 [问题反馈 / Issue Reports](https://github.com/issues)
- 💡 [功能建议 / Feature Requests](https://github.com/discussions)
- 📚 [算法论文 / Algorithm Papers](https://en.wikipedia.org/wiki/Adjusted_winner_procedure)

## 📄 许可证 / License

```
MIT License

Copyright (c) 2025 Room Rent Allocation System

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

**🎉 感谢使用房间房租分配系统！让公平分配变得简单！**  
**🌟 Thank you for using the Room Rent Allocation System! Making fair allocation simple!** 

[![Made with ❤️](https://img.shields.io/badge/Made%20with-❤️-red.svg)](https://github.com)
[![Powered by JavaScript](https://img.shields.io/badge/Powered%20by-JavaScript-yellow.svg)](https://javascript.com/)
[![Open Source](https://img.shields.io/badge/Open%20Source-💚-brightgreen.svg)](https://opensource.org/)

✨ **Star this repo if you find it helpful!** ✨