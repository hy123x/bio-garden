# OpenClaw → Codex Review Handoff

> 由 OpenClaw（小小怪）完成第一版搭建，供 codex 只读 review。

## 项目实际路径
`/Users/hxy/Documents/ChatGPT/与openclaw协作，完成网站搭建`

## 技术栈
Quartz v5（数字花园 / 知识库静态站点框架）+ Markdown + Node.js

## 启动命令（本地预览）
```bash
cd "/Users/hxy/Documents/ChatGPT/与openclaw协作，完成网站搭建"
npx quartz build --serve   # 构建并启动本地服务器，默认 http://localhost:8080
```

## 构建 / 检查命令
```bash
npx quartz build    # 构建静态站点到 public/
npm run check       # TypeScript 类型检查 + Prettier 格式检查
npm run format      # Prettier 格式化
```

环境要求：Node.js ≥ 22（本机 v25.9.0 已验证通过）

## 已完成的页面和功能
- **框架**：Quartz v5 数字花园，站点标题「生物知识花园」，绿色主题配色
- **首页** `content/index.md`：站点介绍 + 三大板块导航
- **三大板块**：
  - 研究生生活 `content/grad-life/`（示例笔记：如何高效读文献）
  - 实验技巧 `content/protocols/`（示例笔记：Western Blot 避坑指南）
  - 基因功能 `content/genes/`（示例笔记：HSPA12A）
- **内容**：共 7 篇 Markdown，含 frontmatter（title / description / tags / aliases / date）与双向链接
- **站点功能**：知识图谱、全文搜索、双向链接、标签页、别名重定向、深色模式、RSS、站点地图、目录
- **部署**：`.github/workflows/deploy.yml`（GitHub Pages Actions 部署，触发分支 main）

## 仍未完成的事项
- 尚未部署上线（本地构建已验证通过，但未推送到 GitHub Pages）
- 内容为示例 / 脚手架性质，待填充真实知识
- HSPA12A 笔记的「文献线索」部分待补充
- 未配置自定义域名（baseUrl 暂为 `hy123x.github.io/bio-garden`，需按实际部署地址确认）
- 未开启站内评论（giscus 默认关闭）

## 重点希望 review 的部分
1. **content/ 7 篇 Markdown**：中文内容质量与专业性、frontmatter 写法、标签体系是否合理、双向链接用法是否正确
2. **三大板块划分**（grad-life / protocols / genes）是否合理、是否便于后续扩展
3. **HSPA12A 笔记** 结构是否适合作为后续「基因功能」笔记的通用模板
4. **quartz.config.yaml**：插件启停是否合理（有无该开没开 / 该关没关的）、主题配色、locale 设置
5. **.github/workflows/deploy.yml**：GitHub Pages 部署工作流是否规范

## 预览地址
- 本地预览：http://localhost:8080（运行 `npx quartz build --serve` 后）
- 线上地址：暂无（未部署）

---

⚠️ 请勿把密码、API Key 或其他敏感信息写入本文件。
