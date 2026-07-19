# TechSupport

FlClash for iOS 技术支持官网 — 用于 App Store Connect 的 **技术支持网址** 与 **隐私政策网址**。

纯静态站点，无构建步骤、无外部依赖。

## 文件结构

**英文为默认语言**：根路径 `index.html` / `privacy.html` 提供英文，中文为 `-zh` 后缀，
两侧页面右上角的语言胶囊互相切换。

```
index.html        English homepage（默认落地页）
index-zh.html     中文首页（功能 / 系统要求 / 常见问题）
privacy.html      English privacy policy（默认）
privacy-zh.html   中文隐私政策
assets/style.css  样式（Apple 风格，自适应深浅色与移动端）
assets/icon.svg   应用图标
```

## 本地预览

```bash
python3 -m http.server 8000
# 打开 http://localhost:8000
```

## 部署到 GitHub Pages

推送到 `main` 后，在仓库 **Settings → Pages** 中将 Source 设为
`Deploy from a branch`，分支选 `main`、目录选 `/ (root)`，保存即可。

站点地址：`https://starhubinfo.github.io/TechSupport/`

## App Store Connect 填写

| 字段 | 值 |
|---|---|
| 技术支持网址 Support URL | `https://starhubinfo.github.io/TechSupport/` |
| 隐私政策网址 Privacy Policy URL | `https://starhubinfo.github.io/TechSupport/privacy.html` |

## 需要同步维护的内容

- **联系邮箱** — 当前为 `info@starhubinformation.com`，仅出现在两份隐私政策的末尾。首页无联系模块。
- **版本号** — 应用发版后更新 `index.html` / `index-zh.html` 中的 `1.0.0`。
- **隐私政策更新日期** — 内容变更时同步修改两份 privacy 页面顶部的日期。
