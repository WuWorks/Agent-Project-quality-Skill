# Project Quality Governance

一套面向 Codex 与工程 Agent 的开源质量治理 Skill，用于建立清晰、可检索、可验证的技术规范与质量日志体系。

它不会替你编写普通产品文案，也不会覆盖已有项目历史。Skill 会先检查仓库现有结构，再以最小改动建立权威规范、Bug/优化记录、分层验收和自动文档校验。

## 核心能力

- 将不可违反的安全、数据和范围规则放在技术规范顶部。
- 建立可点击目录与“任务类型 → 必读章节”路由，减少重复上下文读取。
- 保持稳定的单 H1、H2/H3 文档层级。
- 分离当前规则、已验证事实、历史计划与私有实验资料。
- 为 Bug 与优化建立不同字段，并维护统一状态索引。
- 支持历史追加、事实更正、替代关系和发布说明候选。
- 使用 L1/L2/L3 分层验收，兼顾开发效率与质量。
- 提供只读校验器，检查标题、ID、字段、证据和时间一致性。

## 目录结构

```text
project-quality-governance/
├─ SKILL.md
├─ README.md
├─ LICENSE
├─ agents/
│  └─ openai.yaml
├─ references/
│  ├─ technical-spec-architecture.md
│  ├─ issue-and-improvement-log.md
│  └─ verification-workflow.md
└─ scripts/
   ├─ validate-quality-docs.mjs
   └─ validate-quality-docs.test.mjs
```

## 安装

```bash
git clone https://github.com/WuWorks/Agent-Project-quality-Skill.git
```

将仓库文件夹复制到你的 Codex skills 目录，然后重启 Codex。也可以直接打开 `SKILL.md` 查看适用范围和工作流程。

## 使用方式

```text
使用 project-quality-governance 审查并优化当前项目的技术规范、Bug/优化日志和验证流程。
```

Skill 默认跟随目标项目的语言生成文档；其自身使用英文编写，方便在不同语言和工程环境中复用。

## 文档校验器

校验器只读取显式指定的文件并输出诊断，不会自动改写文档：

```bash
node scripts/validate-quality-docs.mjs \
  --spec path/to/technical-spec.md \
  --log path/to/change-log.md
```

通过 `--config path/to/config.json` 可以配置 ID 前缀、类型和内容标签、完成状态、必填字段、发布文案要求，以及编号章节和允许的非编号 H2。

运行校验器测试：

```bash
node --test scripts/validate-quality-docs.test.mjs
```

## 适用范围

适合创建、审查或重构权威技术规范、Bug 与优化日志、工程质量流程、分层验收规则和文档一致性检查。

不适用于普通营销文案、无结构随手笔记或与工程质量治理无关的内容编辑。

## 隐私与边界

Skill 不要求上传项目文件，不读取未授权的私有研究或密钥，也不会为了补全文档而虚构历史时间与验证证据。

## License

Released under the [Apache License 2.0](LICENSE).
