# Function Extraction

[![skills.sh](https://skills.sh/b/addxing/function-extraction)](https://skills.sh/addxing/function-extraction)

面向 AI 编程代理的功能链路提取 Skill。它可以从项目代码中提取某个具体功能的完整实现链路，并生成包含业务逻辑、数据流、异常处理、模块依赖和 Mermaid 图表的技术开发文档。

## 安装

```bash
npx skills add addxing/function-extraction
```

### DeepSeek Harness

本仓库遵循 DeepSeek Harness（DSH）的 Skill 格式，克隆到技能目录后即可被自动发现：

```bash
# 用户级安装（所有项目可用）
git clone https://github.com/addxing/function-extraction ~/.dsh/skills/function-extraction

# 项目级安装（仅当前项目可用）
git clone https://github.com/addxing/function-extraction .dsh/skills/function-extraction
```

克隆后 DSH 会自动热更新技能目录，新会话即可使用该 Skill。

也可以作为官方 bundle 插件一行安装（需要 pnpm，安装后重启 Web）：

```bash
dsh plugin --profile web add "github:addxing/function-extraction#main"
```


## 使用方式

安装后，在需要提取某个功能实现文档时，让 AI 代理使用这个 Skill：

```text
Use $function-extraction to document the login flow implementation.
```

为了获得更准确的结果，建议提供：

- 功能名称
- 入口文件、类、方法、路由、页面、按钮文案或其他线索
- 如需调整默认输出，说明期望的文档范围或输出语言

如果没有提供入口点，Skill 会指导代理先搜索代码库，并让你确认正确入口后再继续分析。

## 功能说明

这个 Skill 会指导代理：

- 确认目标功能和入口点
- 从入口追踪到功能流程结束
- 识别关键业务逻辑、数据流、状态变化和异常处理
- 使用 `template.md` 生成技术开发文档
- 在适用时输出 Mermaid 流程图、时序图和模块依赖图

## 文件说明

- `SKILL.md` - Skill 指令
- `template.md` - 输出文档模板
- `LICENSE.txt` - Apache 2.0 许可证
