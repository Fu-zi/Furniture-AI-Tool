# Furniture-AI-Tool
AI Sofa Matching + WeChat Furniture Catalog Demo

这是一个已脱敏的开源演示项目合集，包含两个家具/沙发相关 Demo：

1. AI Sofa Matching Demo
    一个用于上传客厅照片、选择沙发产品，并通过可配置后端服务提交 AI 图像编辑任务的 Web 应用示例。
2. WeChat Furniture Catalog Demo
    一个原生微信小程序示例，用于展示家具/沙发图册类小程序的页面结构、筛选交互、详情页、活动页和联系页。

本仓库适合作为家具零售、沙发展示、AI 家居搭配、微信图册小程序等场景的开源参考项目。

项目脱敏说明

本仓库已完成公开发布前的脱敏处理：

* 真实产品图片已替换为生成的占位图或示例图片
* 真实产品目录数据已替换为 Demo 数据
* 品牌信息、地址、电话、公众号文章链接等敏感内容已替换或移除
* API keys、环境变量、本地数据库、上传文件和私有 PRD 内容已移除
* AI 服务 Provider Endpoint 可通过 backend/.env 或后台管理面板配置
* 项目不包含真实客户、真实产品、真实联系方式或真实业务资产

应用组成

AI Sofa Matching Demo

* Customer app: frontend
    基于 Vite + React 的客户前端，用于上传客厅照片、选择沙发产品和提交 AI 编辑任务。
* Admin app: admin-frontend
    基于 Vite 的后台管理前端，用于管理配置、查看任务或维护演示数据。
* Backend API: backend
    基于 Express + SQLite CLI 的后端 API，用于处理账号、产品、任务和 Provider 配置。

WeChat Furniture Catalog Demo

* Mini Program app
    原生微信小程序项目，不依赖 uni-app、Taro 等跨端框架。
* Local mock data
    使用本地 mock 数据，可直接在微信开发者工具中导入运行。
* Main package + subpackage structure
    保留主包与分包结构示例，适合继续替换为真实业务资源。

功能特点

Web / AI Matching Demo

* 上传客厅照片
* 选择沙发产品
* 提交 AI 图像编辑任务
* 支持可配置 AI Provider
* 包含客户前端、后台前端和后端 API
* 默认 Demo 账号可用于快速体验
* 适合扩展为 AI 家居搭配、AI 换沙发、AI 产品预览等场景

WeChat Mini Program Demo

* 原生微信小程序语法
* 首页、产品图册、活动页、联系我们等页面示例
* 产品筛选交互
* 产品详情页
* 活动卡片与活动页
* 联系方式页面
* 公共组件拆分
* 本地 mock 数据，可直接运行
* 适合替换为真实品牌、真实产品和真实业务数据

快速开始

AI Sofa Matching Demo

npm run install:all
cp backend/.env.example backend/.env
npm run start:backend
npm run start:frontend
npm run dev --prefix admin-frontend

后端首次启动时会自动写入默认 Demo 账号：

* Store user: test / msm2026
* Admin user: admin / msmadmin2026

WeChat Furniture Catalog Demo

1. 使用微信开发者工具打开微信小程序项目目录。
2. AppID 可使用测试号，或在 project.config.json 中替换为自己的 AppID。
3. 如需使用真实图片和数据，请替换以下目录中的示例内容：

data/
assets/images/
pkg/p1/assets/

目录说明

.
├── frontend/             # AI Sofa Matching 客户端前端，Vite + React
├── admin-frontend/       # AI Sofa Matching 后台管理前端，Vite
├── backend/              # Express + SQLite 后端 API
├── pages/                # 微信小程序页面：首页、产品图册、活动、联系我们等
├── components/           # 微信小程序公共组件：产品卡片、活动卡片、标题区块、咨询条等
├── data/                 # 脱敏后的品牌、产品、活动和联系方式 mock 数据
├── assets/images/        # 微信小程序主包公共图片与 tabBar 图标
└── pkg/p1/               # 微信小程序产品详情分包示例

实际目录结构可根据仓库组织方式调整。如果 Web Demo 和小程序 Demo 位于不同子目录，建议分别放在 ai-sofa-matching-demo/ 与 wechat-furniture-catalog-demo/ 下。

环境变量与配置

AI Sofa Matching Demo 的后端配置位于：

backend/.env

可参考示例文件：

backend/.env.example

Provider endpoints、API keys 和其他本地配置应通过 .env 或后台管理面板配置，不应提交到 Git 仓库。

安全注意事项

请勿提交以下内容：

backend/.env
backend/data/
uploaded files
provider API keys
real customer assets
real product assets
real addresses
real phone numbers
private PRD content
local databases

建议在提交前检查 .gitignore，确保本地数据库、上传文件、环境变量和真实业务资源不会被误提交。

替换为真实业务资源

如需基于本项目开发真实业务版本，可替换以下内容：

* 产品图片
* 产品名称、型号、分类、材质、颜色、价格等数据
* 品牌介绍
* 门店地址
* 联系电话
* 小程序 AppID
* 公众号文章链接
* AI Provider Endpoint
* 后端数据库
* 用户系统与权限配置

注意

本项目仅为开源演示版本，用于展示 AI 沙发搭配 Web 应用和微信家具图册小程序的基本结构与交互方式。

本项目不包含真实品牌、真实产品、真实客户数据、真实地址、真实联系方式或任何私有业务内容。
