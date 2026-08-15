# 山月集 · 个人博客

一个单文件 HTML 个人博客，无需构建、无需后端，可直接部署到 GitHub Pages。

## 功能特性

- 文章与网页链接两种内容类型
- 游客模式 / 管理员模式（管理员需密码，支持增删改、导出博客）
- 深色 / 浅色主题切换
- 文章搜索、热门文章、标签云
- 内容中的 URL 自动识别（Ctrl + 单击打开）
- 数据保存在浏览器 localStorage
- 响应式布局，支持移动端
- 可将当前数据导出为独立 HTML 文件

## 快速开始

本地打开 `index.html` 即可使用（数据保存在浏览器 localStorage 中）。

## 部署到 GitHub Pages

1. 在 GitHub 上新建仓库（如 `shanyue-ji`），将本目录文件推送上去：

   ```bash
   git init
   git add .
   git commit -m "init: 山月集个人博客"
   git branch -M main
   git remote add origin https://github.com/<你的用户名>/<仓库名>.git
   git push -u origin main
   ```

2. 进入仓库 **Settings → Pages**，将 Source 设为 `Deploy from a branch`，分支选 `main`，目录选 `/ (root)`，保存。
3. 等待约 1 分钟，访问 `https://<你的用户名>.github.io/<仓库名>/` 即可。

## 安全提示

> ⚠️ 管理员密码以明文写在 `index.html` 的 JavaScript 中（`ADMIN_PASSWORD` 常量）。
> 部署到 GitHub Pages 后任何人都能查看网页源代码获取该密码。
> 建议上传前修改密码，或仅将本工具作为个人演示使用。

## 目录结构

```
shanyue-ji/
└── index.html   # 单文件博客（HTML + CSS + JS 全部内嵌）
```

## 许可证

仅供个人学习与使用。