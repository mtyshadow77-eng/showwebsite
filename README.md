# 游戏策划 - 王臧伟 个人网站

## 项目介绍

这是一个展示游戏策划师王臧伟个人信息、项目经验和专业技能的前端网站。

## 技术栈

- HTML5
- Tailwind CSS
- JavaScript
- Font Awesome

## 部署指南

### 1. 部署到GitHub Pages

#### 步骤：

1. 在GitHub上创建一个新的仓库
2. 将本项目的文件推送至仓库
3. 启用GitHub Actions：
   - 仓库 → Settings → Actions → General → 确保"Allow all actions and reusable workflows"已启用
4. 配置GitHub Pages：
   - 仓库 → Settings → Pages → Build and deployment → Source → 选择"GitHub Actions"
5. 推送代码到main分支，GitHub Actions会自动部署网站

### 2. 使用自定义域名和Cloudflare加速

### 步骤1：配置GitHub Pages自定义域名

1. 在项目根目录创建`CNAME`文件，内容为：
   ```
   mtyshadow.show.com
   ```
2. 推送`CNAME`文件到GitHub仓库
3. 进入GitHub仓库 → Settings → Pages
4. 在"Custom domain"部分，输入`mtyshadow.show.com`
5. 点击"Save"，GitHub会自动验证域名

### 步骤2：配置Cloudflare

1. 注册Cloudflare账号
2. 添加站点：
   - 输入`mtyshadow.show.com`
   - 按照提示完成DNS设置
3. 配置DNS记录：
   - 添加CNAME记录：
     - 名称：`mtyshadow.show.com`
     - 内容：`your-username.github.io`（替换为你的GitHub Pages域名）
     - 代理状态：开启（橙色云朵图标）
4. 启用CDN加速：
   - 在Cloudflare控制面板中，确保CDN已启用
   - 检查缓存设置，确保静态资源被正确缓存
5. 启用HTTPS：
   - 在Cloudflare控制面板中，启用"Always Use HTTPS"
   - 确保SSL/TLS设置为"Flexible"或"Full"
6. 配置页面规则：
   - 添加页面规则：`mtyshadow.show.com/*` → 缓存级别：缓存所有内容
   - 启用"Rocket Loader"和"HTTP/3 (QUIC)"以优化性能

### 3. 国内访问优化

#### 建议：

- 确保Cloudflare的CNAME记录已正确设置
- 启用Cloudflare的" Rocket Loader"功能以加速JavaScript加载
- 考虑使用Cloudflare的" Argo Smart Routing"功能（需付费）以获得更好的国内访问速度

## 本地开发

### 启动本地服务器

```bash
# 使用Python
python -m http.server 8000

# 或使用http-server
npx http-server -p 8000
```

然后访问 `http://localhost:8000` 查看网站。

## 文件结构

```
├── index.html          # 主页面
├── README.md           # 项目说明
└── .github/
    └── workflows/
        └── deploy.yml  # GitHub Actions部署配置
```

## 联系信息

如有任何问题，欢迎联系：

- 邮箱：[3032825203@qq.com](mailto:your-email@example.com)
- GitHub：mtyshadow77-eng

