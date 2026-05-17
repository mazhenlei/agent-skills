# Agent Skills

opencode agent 技能集合。

## Skills 列表

| Skill | 说明 | 安装命令 |
|-------|------|---------|
| android-modularize | Android 项目组件化迁移 | `opencode skill add https://github.com/mazhenlei/agent-skills.git android-modularize` |

## android-modularize

Android 项目组件化迁移技能，用于将单体 app 模块中的业务代码逐步拆分到独立业务模块，实现组件化架构。

### 功能

- 自动探测项目配置（路由方案、模块命名风格、基础模块等）
- 逐步拆分业务模块，每次只拆一个，拆完验证再拆下一个
- 生成模块模板代码和目录结构
- 配置模块间路由通信
- 处理模块间依赖关系

### 使用

安装后，在 opencode 中提到"组件化"、"模块拆分"、"拆模块"等关键词即可自动触发该技能。

### 触发关键词

组件化、模块拆分、模块化、拆模块、迁移业务代码、抽模块、解耦、独立编译

### 没有 opencode 也能用

SKILL.md 本质上是一套完整的组件化迁移指南和模板，不依赖 opencode 也能使用：

**1. 直接阅读文档**

直接阅读 `android-modularize/SKILL.md` 及 `references/` 下的参考文档，按指南手动操作。

**2. 配合 Cursor**

将 `SKILL.md` 内容放到项目的 `.cursor/rules/` 目录下，Cursor 会自动读取并遵循其中的迁移规范。

**3. 配合 Claude Code**

将 `SKILL.md` 内容追加到项目根目录的 `CLAUDE.md` 文件中，Claude Code 会作为项目指令自动加载。

**4. 配合其他 AI 编码工具**

将 `SKILL.md` 内容作为 system prompt 或自定义指令喂给任何 AI 编码工具，即可获得组件化迁移的指导。

## 目录结构

```
├── README.md
├── android-modularize/       # Android 组件化迁移技能
│   ├── SKILL.md
│   ├── references/
│   └── scripts/
├── <new-skill>/              # 后续新增技能
│   ├── SKILL.md
│   └── ...
```

## License

MIT
