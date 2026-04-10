# 专辑完结审核平台 · 静态原型

本仓库为 HTML/CSS/JS 静态原型，可托管于 **GitHub Pages**，供外部访问。

## 在线访问地址（部署完成后）

将 `YOUR_REPO` 替换为你在 GitHub 上创建的仓库名，例如 `audit-platform`：

- **首页（自动进入审核列表）**：`https://fahrenheityue-pixel.github.io/YOUR_REPO/`
- **审核列表**：`https://fahrenheityue-pixel.github.io/YOUR_REPO/audit-list-prototype.html`

管理员演示：在审核列表 URL 后加 `?admin=1`。

## 首次发布到 GitHub（在你本机终端执行）

### 1. 在 GitHub 网页上新建仓库

1. 登录 GitHub，打开 <https://github.com/new>
2. Repository name 填写例如：`audit-platform`（名称可自定）
3. 可见性选 **Public**（GitHub Pages 免费版对私有仓库有限制，公开仓库最省事）
4. **不要**勾选「Add a README」，创建空仓库

### 2. 推送本地代码

在终端进入本目录（含 `index.html` 与各页面文件），执行（把 `audit-platform` 改成你的仓库名）：

```bash
cd /path/to/audit-platform-github
git init
git add .
git commit -m "Initial commit: audit platform static prototype"
git branch -M main
git remote add origin https://github.com/fahrenheityue-pixel/audit-platform.git
git push -u origin main
```

若已配置 SSH，可将 `remote` 改为：

`git@github.com:fahrenheityue-pixel/audit-platform.git`

### 3. 开启 GitHub Pages

1. 打开仓库 → **Settings** → **Pages**
2. **Build and deployment** → Source：**Deploy from a branch**
3. Branch：**main**，文件夹：**/ (root)**
4. Save。等待 1～3 分钟后访问上述 URL。

## 文件说明

| 文件 | 说明 |
|------|------|
| index.html | 入口，跳转到审核列表 |
| audit-list-prototype.html | 审核列表主页面 |
| ticket-detail.html | 机审工单详情 |
| human-audit-*.html | 人审各渠道页面 |
| appeal-ticket-view.html | 申诉查看 |
| admin-audit-result.html | 管理员修改审核结果 |

## 说明

- 原型中部分能力使用浏览器 `sessionStorage`，不同访客数据互不干扰。
- Excel 导入依赖外链 JS（SheetJS CDN），需联网加载。
