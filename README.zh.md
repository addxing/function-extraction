# Function Extraction

[![skills.sh](https://skills.sh/b/addxing/function-extraction)](https://skills.sh/addxing/function-extraction)

面向 Codex/AI 编程代理的功能链路提取 Skill。它可以从项目代码中提取某个具体功能的完整实现链路，并生成包含业务逻辑、数据流、异常处理、模块依赖和 Mermaid 图表的技术开发文档。

## 安装

```bash
npx skills add addxing/function-extraction
```

## 使用方式

安装后，在需要提取某个功能实现文档时，让 Codex 使用这个 Skill：

```text
Use $function-extraction to document the login flow implementation.
```

为了获得更准确的结果，建议提供：

- 功能名称
- 入口文件、类、方法、路由、页面、按钮文案或其他线索
- 如需调整默认输出，说明期望的文档范围或输出语言

如果没有提供入口点，Skill 会指导 Codex 先搜索代码库，并让你确认正确入口后再继续分析。

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
- `agents/openai.yaml` - Codex UI 元数据
- `LICENSE.txt` - Apache 2.0 许可证
