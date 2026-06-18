# 🤖 AI 应用导航

> 精选全球顶级 AI 工具，分类导航，一站发现最好的 AI 应用。

**在线地址：** https://z243069942.github.io/ai-nav/

---

## ✨ 功能特色

- 🗂️ **10 大分类**：对话、图像、编程、写作、视频、音频、搜索、效率、设计、研究
- 🔍 **实时搜索**：快速检索 50+ 精选 AI 应用
- ⭐ **精选过滤**：一键筛选精选 / 免费 工具
- ⚙️ **管理后台**：通过 GitHub API 直接增删改查，无需服务器

---

## 🚀 快速部署

### 第一步：Fork 本仓库

点击右上角 **Fork** 按钮 → 仓库名保持 `ai-nav`

### 第二步：启用 GitHub Pages

1. 进入仓库 **Settings** → **Pages**
2. Source 选择 **Deploy from a branch**
3. Branch 选 **main**，文件夹选 **/ (root)**
4. 点击 **Save**

约 1 分钟后，网站部署完成：`https://<你的用户名>.github.io/ai-nav/`

---

## 🔑 管理后台使用方法

### 获取 GitHub Token

1. 访问 [GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)](https://github.com/settings/tokens/new)
2. 勾选 **repo** 权限
3. 生成并复制 Token（只显示一次，请妥善保存）

### 登录后台

1. 打开 `https://<你的用户名>.github.io/ai-nav/admin.html`
2. 填写：
   - **GitHub 用户名**：你的 GitHub 用户名
   - **仓库名**：`ai-nav`
   - **分支**：`main`
   - **Token**：粘贴你的 Personal Access Token
3. 点击「连接 GitHub」

### 后台功能

| 功能 | 说明 |
|------|------|
| ➕ 添加应用 | 填写名称、URL、分类、描述、标签 |
| ✏️ 编辑应用 | 修改已有应用信息 |
| 🗑️ 删除应用 | 删除应用（即时同步到 GitHub） |
| 📁 分类管理 | 添加/编辑/删除分类 |
| 📥 导出 JSON | 下载完整数据备份 |
| 📤 导入 JSON | 批量导入应用数据 |

---

## 📁 项目结构

```
ai-nav/
├── index.html      # 主页（导航展示）
├── admin.html      # 管理后台
├── data.json       # 数据文件（分类 + 应用）
└── README.md       # 本说明文件
```

---

## 🛠️ 本地开发

```bash
# 克隆仓库
git clone https://github.com/z243069942/ai-nav.git
cd ai-nav

# 启动本地服务（任选其一）
python -m http.server 8080
# 或
npx serve .
```

打开 http://localhost:8080 即可预览。

---

## 📄 数据格式

### 应用 (apps)

```json
{
  "id": "唯一ID",
  "name": "应用名称",
  "url": "https://...",
  "category": "分类ID",
  "description": "简短描述",
  "icon": "图标URL（可选）",
  "tags": ["标签1", "标签2"],
  "featured": true
}
```

### 分类 (categories)

```json
{
  "id": "分类ID（英文）",
  "name": "显示名称",
  "icon": "🎨",
  "description": "分类描述"
}
```

---

## 📝 License

MIT © 2025
