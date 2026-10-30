# 软考知径 · 2027 软考中级备考系统精讲站

一个面向 **2027 年度计算机技术与软件专业技术资格（水平）考试 · 中级（系统集成项目管理工程师）** 的静态学习网站。按知识域顺序系统精讲，覆盖全部核心章节，并配套备考时间表与案例实战。

## 站点结构

系统精讲路线图（学习顺序）：

> 总览 → 信息化与发展 → 信息技术基础 → 项目管理基础 → 立项管理 → 整体与范围管理 → 进度与成本管理（计算核心） → 质量/人力资源/沟通管理 → 风险与干系人管理 → 采购与合同管理 → 配置与变更管理 → 法律法规/标准规范/专业英语 → 案例分析实战

每章下设若干**子专题**细化讲义，父章页自动汇总「本章子专题」。

## 目录说明

```
RK2027/
├── build.py                 # 静态站生成器（Markdown → dist/）
├── src/                     # 模板与资源
│   ├── index.html           # 首页（学习路线图悬窗 + 进度勾选）
│   ├── topic.html           # 专题页模板
│   └── assets/              # CSS / JS
├── content/topics/          # 内容源（Markdown，在这里写笔记）
├── dist/                    # 构建产物（被 .gitignore 忽略，CI 会重建）
└── .github/workflows/       # GitHub Pages 自动部署
```

## 本地使用

需要 Python 3 与 `markdown` 库：

```bash
pip install markdown
python build.py          # 生成 dist/
python -m http.server 8000 -d dist   # 本地预览
```

- 补笔记：直接编辑 `content/topics/*.md`，再运行 `build.py`。
- 新增子专题：在 `content/topics/` 新建 `.md` 并加 `parent: <父章slug>`，父章页会自动汇总。

## 部署

仓库已内置 GitHub Pages 工作流（`.github/workflows/deploy.yml`）：推送 `main` 分支即自动构建并发布。
在仓库 **Settings → Pages** 中将 Source 设为 **GitHub Actions** 即可。

> 注：本站内容仅供个人备考学习参考，具体报考政策、考试大纲与合格标准以工业和信息化部教育与考试中心官方公告为准。
