# Hunyuan3D AI 3D模型生成器

一个简洁优雅的Web界面，用于将2D图片转换为3D模型。

## 🚀 快速部署到Vercel

### 方式1：通过Vercel CLI

```bash
# 安装Vercel CLI
npm install -g vercel

# 在项目目录中部署
cd ~/Desktop/hunyuan3d-web
vercel
```

### 方式2：通过GitHub + Vercel网页

1. 将代码推送到GitHub仓库
2. 访问 [vercel.com](https://vercel.com)
3. 点击 "New Project"
4. 导入您的GitHub仓库
5. 点击 "Deploy"

## 📝 配置说明

### 修改API地址

如果您的Cloudflare Tunnel URL变化了，请修改 `index.html` 中的API地址：

```javascript
// 找到这一行并替换为您的新URL
const API_URL = 'https://observer-payday-contest-median.trycloudflare.com';
```

## 🎨 功能特点

- ✅ 拖拽上传图片
- ✅ 实时进度显示
- ✅ 3D模型在线预览
- ✅ 一键下载模型
- ✅ 响应式设计
- ✅ 参数可调整

## 🔧 本地测试

直接用浏览器打开 `index.html` 文件即可。

## 📦 项目结构

```
hunyuan3d-web/
├── index.html      # 主页面
├── vercel.json     # Vercel配置
└── README.md       # 说明文档
```

## 🌐 架构说明

```
用户 → Vercel (前端)
     ↓ API调用
     Cloudflare Tunnel → Mac mini (后端AI服务)
```

## 📱 使用方法

1. 上传一张图片
2. (可选) 调整生成参数
3. 点击"生成3D模型"
4. 等待几分钟
5. 在线预览或下载GLB文件

## ⚠️ 注意事项

- Cloudflare Quick Tunnel的URL在重启后会变化
- 如需稳定的URL，请使用Cloudflare Named Tunnel
- 生成时间取决于您的Mac mini性能（通常5-30分钟）

## 🔒 安全提示

- 当前未设置访问限制
- 建议添加简单的密码保护
- 监控API调用频率

## 📄 许可证

MIT
