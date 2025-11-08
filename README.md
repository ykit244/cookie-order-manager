# 🍪 饼干订单管理系统 PWA

妈妈的手工饼干订单管理小助手 - 一个支持离线使用的渐进式网页应用

## 📱 功能特点

- ✅ 订单管理（添加、编辑、删除、状态追踪）
- ✅ 客户管理（保存常客信息）
- ✅ 产品管理（维护产品列表和价格）
- ✅ 智能提醒（3天内到期订单自动提醒）
- ✅ 数据持久化（localStorage 本地存储）
- ✅ PWA 支持（可安装到主屏幕，离线使用）
- ✅ 响应式设计（手机和电脑都能使用）

## 🚀 快速开始

### 方法1：直接打开 HTML 文件

1. 双击 `index.html` 文件在浏览器中打开
2. 就这么简单！

### 方法2：使用本地服务器（推荐）

PWA 功能需要 HTTPS 或 localhost 环境才能正常工作。

#### 使用 Python（如果已安装）

```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

然后访问：http://localhost:8000

#### 使用 Node.js

```bash
# 安装 http-server（全局安装一次即可）
npm install -g http-server

# 运行服务器
http-server -p 8000
```

然后访问：http://localhost:8000

## 📦 部署到网络（推荐）

### 使用 Vercel（免费且简单）

1. **注册 Vercel**
   - 访问 https://vercel.com
   - 使用 GitHub/GitLab/Bitbucket 账号登录

2. **上传项目到 GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin YOUR_GITHUB_REPO_URL
   git push -u origin main
   ```

3. **在 Vercel 导入项目**
   - 点击 "New Project"
   - 导入你的 GitHub 仓库
   - 点击 "Deploy"
   - 等待部署完成，获得网址（例如：cookie-app.vercel.app）

4. **配置自定义域名（可选）**
   - 在 Vercel 项目设置中添加你的域名

### 使用 Netlify（也很简单）

1. 访问 https://netlify.com
2. 拖拽整个文件夹到 Netlify Drop
3. 立即获得一个网址

### 使用 GitHub Pages（完全免费）

1. 创建一个名为 `username.github.io` 的仓库
2. 上传所有文件到仓库
3. 访问 https://username.github.io

## 📱 安装到手机主屏幕

部署到网络后：

### iOS (Safari)

1. 在 Safari 中打开网址
2. 点击底部的"分享"按钮
3. 向下滚动，选择"添加到主屏幕"
4. 点击"添加"

### Android (Chrome)

1. 在 Chrome 中打开网址
2. 点击右上角菜单（三个点）
3. 选择"添加到主屏幕"
4. 点击"添加"

完成后，手机桌面会出现一个图标，点击后全屏打开，体验接近原生 app！

## 🎨 自定义图标

目前使用的是占位图标。如果想自定义图标：

1. 准备两个 PNG 图片：
   - `icon-192.png` (192x192 像素)
   - `icon-512.png` (512x512 像素)

2. 将图片放在与 `index.html` 同一目录下

3. 建议使用简单、清晰的设计（例如：🍪 饼干图标）

可以使用在线工具生成图标：
- https://www.pwa-icon-generator.com/
- https://favicon.io/

## 🔧 文件说明

```
cookie-order-app/
├── index.html              # 主应用文件（包含完整的 React 应用）
├── manifest.json           # PWA 配置文件
├── service-worker.js       # Service Worker（离线功能）
├── icon-192.png           # 应用图标 (192x192)
├── icon-512.png           # 应用图标 (512x512)
└── README.md              # 说明文档（本文件）
```

## 💾 数据存储

- 所有数据保存在浏览器的 localStorage 中
- 即使关闭浏览器或重启手机，数据依然保留
- 数据仅存储在本地，不会上传到服务器
- 如果清除浏览器数据，订单信息会丢失（建议定期备份）

## 🆘 常见问题

**Q: 为什么我的数据丢失了？**
A: 可能是清除了浏览器缓存。建议定期截图或导出重要订单信息。

**Q: 可以在多个设备上同步数据吗？**
A: 当前版本使用本地存储，不支持多设备同步。如需此功能，需要添加后端数据库。

**Q: Service Worker 没有注册成功？**
A: 确保使用 HTTPS 或 localhost 访问。直接打开 HTML 文件无法使用 Service Worker。

**Q: 如何更新应用？**
A: 如果部署到网络，只需更新代码并重新部署。用户刷新页面即可获得更新。

## 📝 待优化功能

- [ ] 数据导出（CSV/Excel）
- [ ] 数据备份和恢复
- [ ] 多设备云同步
- [ ] 销售统计和图表
- [ ] 打印订单功能
- [ ] 批量操作

## 🤝 技术支持

如有问题或建议，欢迎联系！

## 📄 许可证

本项目仅供个人使用。
