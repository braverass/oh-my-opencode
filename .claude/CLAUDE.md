# Oh My OpenCode 配置

> **项目**: oh-my-opencode
> **仓库**: https://github.com/code-yeongyu/oh-my-opencode
> **作者**: YeonGyu-Kim
> **版本**: 3.1.6

## 项目概述

The Best AI Agent Harness - 开箱即用的 OpenCode 插件，支持多模型编排、并行后台 Agent 和精心设计的 LSP/AST 工具。

**核心功能**:
- **多模型编排**: 支持多个 AI 模型协同工作
- **并行后台 Agent**: Oracle、Librarian、Frontend Engineer 等专业 Agent
- **LSP/AST 工具**: 基于语言服务器协议和抽象语法树的代码操作
- **MCP 集成**: 精选的 Model Context Protocol 服务器
- **Claude Code 兼容层**: 完整兼容 Claude Code 功能

## 技术栈

| 技术 | 版本 | 用途 |
|------|------|------|
| Bun | latest | 运行时 / 打包 |
| TypeScript | ^5.7.3 | 主要语言 |
| @opencode-ai/sdk | ^1.1.19 | OpenCode SDK |
| @opencode-ai/plugin | ^1.1.19 | 插件 API |
| @modelcontextprotocol/sdk | ^1.25.1 | MCP 协议 |
| @ast-grep/napi | ^0.40.0 | AST 查询和转换 |
| vscode-jsonrpc | ^8.2.0 | LSP 通信 |

## 项目结构

```
oh-my-opencode/
├── src/              # TypeScript 源代码
├── dist/            # 编译输出
├── bin/             # CLI 入口
├── packages/        # 子包 (Oracle, Librarian 等)
├── script/          # 构建脚本
├── docs/            # 文档
└── .github/         # CI/CD
```

## 开发规范

### 命令
- `bun run build` - 编译项目
- `bun run typecheck` - 类型检查
- `bun test` - 运行测试
- `bun run build:schema` - 构建 JSON Schema
- `bun run build:binaries` - 构建平台二进制文件

### 代码风格
- 使用 Bun 作为构建工具
- TypeScript strict mode
- Zod 用于 schema 验证
- AST-grep 用于代码查询

### 专有 Agent

| Agent | 功能 |
|-------|------|
| Oracle | 代码预测和建议 |
| Librarian | 文档和知识检索 |
| Frontend Engineer | UI/UX 开发 |
| MCP Server | 协议服务器集成 |

## CLI 工具

```bash
oh-my-opencode [command]
```

可用命令见 `bin/oh-my-opencode.js` 和项目文档。

## LSP/AST 工具

基于 `@ast-grep/napi` 的代码操作：
- 代码搜索和替换
- 重构支持
- 语法树遍历

## MCP 服务器集成

支持标准的 MCP 服务器，通过 `@modelcontextprotocol/sdk` 集成。

## 安全警告

⚠️ **冒充网站警告**: `ohmyopencode.com` 与本项目无关。官方下载仅在 GitHub Releases。

⚠️ **Claude OAuth**: Anthropic 已限制第三方 OAuth 访问。本项目不实现任何自定义 OAuth 系统。

## 相关文档

- [README](./README.md) - 完整文档
- [AGENTS.md](./AGENTS.md) - Agent 说明
- [CONTRIBUTING.md](./CONTRIBUTING.md) - 贡献指南
- [CLA.md](./CLA.md) - 贡献者许可协议

---

## 资源索引

详见 `.claude/index.json`

## 历史记录

详见 `.claude/completed.md`

## 当前任务

详见 `.claude/in-progress.md`
