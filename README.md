# Agent Framework Scratch

一个从零手写、可渐进扩展的 **AI Agent 框架** 实验仓库。目标是把「推理循环、工具调用、上下文与记忆」等核心能力拆开实现，便于阅读、替换与二次开发，而不是堆一层黑盒抽象。

## 特性（规划与原则）

- **手写优先**：核心逻辑以可读性为第一目标，避免过度魔法与隐式约定。
- **模块化**：Agent 循环、工具注册、模型适配、记忆等边界清晰，可单测、可替换。
- **可上线路径**：后续可接 CLI、HTTP、队列等入口；本书写仓库侧重核心与示例。

## 在线文档页（GitHub Pages）

本仓库在 `docs/` 下提供静态站点入口，部署后即可在浏览器中打开项目介绍页。

### 部署步骤

1. 将本仓库推送到 GitHub。
2. 打开仓库 **Settings → Pages**。
3. **Build and deployment → Source** 选择 **Deploy from a branch**。
4. **Branch** 选择默认分支（如 `main`），文件夹选 **`/docs`**，保存。

数分钟后，站点地址一般为：

`https://<你的用户名>.github.io/<仓库名>/`

### 入口说明

| 文件 | 作用 |
|------|------|
| `docs/index.html` | GitHub Pages 默认首页；自动跳转到 `index.xml` 对应页面。 |
| `docs/index.xml` | **XHTML** 格式的项目介绍页，可直接访问：`.../index.xml`。 |

若你只关心「用 XML/XHTML 页面打开说明」，请使用：

`https://<你的用户名>.github.io/<仓库名>/index.xml`

### 本地预览

在仓库根目录执行（需安装 Python 3）：

```bash
cd docs
python -m http.server 8765
```

浏览器访问 `http://127.0.0.1:8765/` 或 `http://127.0.0.1:8765/index.xml`。

## 仓库结构（预期）

```
├── README.md           # 本说明
├── docs/               # GitHub Pages 静态页（index.html + index.xml）
└── ...                 # 框架源码与示例（随开发补充）
```

## 开源协议

MIT License（若尚未添加 `LICENSE` 文件，可自行补充同名 MIT 全文）。

## 致谢

本地文档页设计风格参考常见技术文档站（侧栏导航、徽章与渐变主题）；实现为独立静态资源，不依赖构建工具。
