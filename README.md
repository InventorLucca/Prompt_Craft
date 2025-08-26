# Prompt_Craft - Minecraft Fabric 模组
一款使用AIAPI自动生成Minecraft命令的Fabric模组～～



> 🌟 用自然语言控制你的 Minecraft 世界 —— Prompt_Craft 让你通过 AI 自动生成并执行游戏指令！

---

## 📌 项目简介

**Prompt_Craft** 是一款为 Minecraft Java 版设计的 Fabric 客户端模组，旨在通过调用主流 AI 大模型 API（ 支持 openai 和 google 的请求格式 ），将玩家输入的自然语言描述**自动转换为有效的 Minecraft 指令**，并提供一键执行功能。

无需记忆复杂命令，只需用中文或英文描述你想要的操作，AI 就能帮你生成精准的 `/give`、`/tp`、`/summon` 等指令，大幅提升游戏效率与创造力。

> ✅ 支持 Fabric | 🖥️ 客户端或服务端（未测试） | 🌐 多语言输入 | 🔐 黑名单保护

---

## 🔧 核心功能

- ✅ **AI 指令生成**
  - 支持 openai 和 google 的请求格式
  - 自动解析自然语言 → 转换为可执行的 Minecraft 命令

- 🎯 **快捷交互界面**
  - 按 `G` 键呼出操作面板（不暂停游戏，类似 HUD 菜单）
  - 界面支持中文与英文双语显示

- ⚙️ **API 配置灵活**
  - 首次使用需配置：
    - API 密钥（Key）
    - 模型名称（如 `gpt-4o`, `deepseek-chat`, `kimi` 等）
    - 自定义 API 调用地址（支持反向代理/本地部署）

- ▶️ **一键执行**
  - 生成指令后点击按钮即可发送至聊天栏或直接执行（需开启作弊权限）

- 🛡️ **智能黑名单系统**
  - 可设置关键词过滤危险指令（如 `/op`, `/kill @a`, `/fill` 大范围破坏等）
  - **服务器环境**：仅房主和管理员可修改配置
  - **单机游戏**：所有玩家默认可自由配置

---

## 📦 安装说明

### 前置依赖
- [Fabric Loader](https://fabricmc.net/use/)（对应版本）
- Java 17+（推荐 Oracle JDK 或 OpenJDK）
- 支持MC版本1.21+

### 安装步骤
1. 下载本项目发布的最新 `.jar` 文件
2. 将文件放入 Minecraft 的 `mods` 文件夹
3. 启动游戏，确保 Fabric 和模组正常加载

> 💡 支持版本：`1.21.1 ~ 1.21.8`（Fabric）

---

## 🚀 使用方法

### 1. 首次配置
进入游戏后按 `G` 打开界面 → 点击“⚙️ 配置” 
（或在modmenu模组设置界面配置）
填写以下信息：
- **API Key**：你的 AI 平台密钥
- **Model Name**：使用的模型（如 `gpt-4o`）
- **Base URL**：自定义 API 地址

### 2. 生成指令
在输入框中用自然语言描述你想做的事，例如：
> “给我一个附魔了效率V和耐久III的钻石镐”

点击“生成”按钮，AI 将返回：
```mcfunction
/give @p diamond_pickaxe{Enchantments:[{id:"minecraft:efficiency",lvl:5},{id:"minecraft:unbreaking",lvl:3}]}
```

### 3. 执行指令
点击“执行”按钮，指令将自动发送到聊天栏（或复制执行，视权限而定）

---

## 🔒 安全与权限

| 场景 | 配置权限 |
|------|----------|
| 单人游戏 | 所有玩家均可修改 API 和黑名单 |
| 多人服务器 | 仅 OP / 管理员可修改设置 |

### 黑名单关键词示例
```txt
/op
/stop
/kill @a
/setblock ~ ~-1 ~ minecraft:lava
```
任何生成的指令若包含黑名单关键词，将被拦截并提示警告。

---

## 🤝 贡献指南

欢迎提交 Bug 报告、功能建议！

### 如何参与
- 🐞 **报告问题**：在 Issues 中提交详细的复现步骤
- 💡 **提出功能**：使用 Feature Request 模板
- 🛠️ **代码贡献**：Fork 项目 → 修改代码 → 提交 PR

> 请遵循代码风格规范，并确保兼容最新 Fabric API。

---

## 📄 许可证

本项目基于 [GNU Affero General Public License v3.0](LICENSE) 开源，允许自由使用、修改和分发、商业用途但禁止闭源发布。

---

## 📬 联系方式

- GitHub Issues: [提交问题](https://github.com/InventorLucca/Prompt_Craft/issues)
- Email: luccazhangg@gmail

---

## 🙌 致谢

感谢以下项目与平台的支持：
- [Fabric API](https://fabricmc.net/)
- OpenAI / DeepSeek / Kimi 大模型服务
- MC百科 提供技术参考

---

> 🎮 让 AI 成为你在方块世界中的得力助手！  
> 立即下载，开启智能指令新体验 👉 [Releases](https://github.com/InventorLucca/Prompt_Craft/releases/)
