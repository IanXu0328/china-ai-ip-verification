# 贡献指南

欢迎为「中国 AI 知识产权判例核验库」贡献内容。本库强调**真实、可核验、结构化、可复用**。

## 仓库结构

```text
.
├── README.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── CHANGELOG.md
├── hallucination-log.md
├── cases/
├── rules/
├── tools/
└── templates/
```

- `cases/`：AI 知识产权判例
- `rules/`：司法规则、部门规章、典型案例通报
- `tools/`：AI 提示词、核验清单、工作流说明
- `templates/`：标准化录入模板
- `hallucination-log.md`：AI 幻觉记录

## 可以贡献什么

- 新增 AI 知识产权判例
- 补充司法规则或部门规章
- 修正案例字段、核验链接、法条引用
- 提交新的 AI 工具链或提示词
- 报告 AI 幻觉
- 改进模板、索引和文档

## 收录原则

案例必须满足以下任一条件：

- 裁判文书网可检索；
- 法院官网、最高法、地方高院官方通报；
- 权威媒体明确报道，且能追溯到法院或裁判文书来源。

不接受仅凭自媒体、短视频、论坛帖子收录的案例。

## 提交新案例流程

1. 复制 `templates/case-template.md`。
2. 按模板填写，重点确认：
   - `case_number`
   - `court`
   - `judgment_date`
   - `verified_source`
   - `verified_url`
   - `verify_status`
3. 在裁判文书网或官方通报中核验案号、法院、判决结果、赔偿金额。
4. 将文件放入 `cases/`，文件名建议为 `case-关键词.md`。
5. 在 `README.md` 中新增一行索引。
6. 在 `CHANGELOG.md` 中记录本次更新。

## 提交方式

1. Fork 本仓库。
2. 创建分支，例如：

```bash
git checkout -b case/ai-voice-clone
```

3. 提交更改。
4. 发起 Pull Request，并在描述中说明：
   - 新增或修改了哪些内容；
   - 核验来源链接；
   - 是否已确认案号和判决结果。

## 案例字段要求

- 案号必须完整、准确；
- 法院名称必须使用全称；
- 判决日期使用 `YYYY-MM-DD` 格式；
- 赔偿金额如无法确认，填写“文书未提及”；
- 核验状态未确认前必须填“待核验”；
- 不得编造法条、案号、判决结果。

## AI 使用规范

本库允许使用 AI 辅助检索、摘要、格式化，但必须遵守：

- AI 输出不能直接入库；
- 所有法条、案号、金额、法院名称必须人工核验；
- 发现 AI 幻觉时，记录到 `hallucination-log.md`；
- 不得把 AI 生成内容伪装成原始裁判文书。

## 提交 Pull Request 前自检

- 是否使用了最新模板；
- 案号、法院、时间是否核验；
- 核验链接是否有效；
- 文件是否放入正确目录；
- 是否更新了 `README.md` 和 `CHANGELOG.md`；
- 是否存在编造内容。

## 通过 Issue 提交线索

如果暂时不方便提交 Pull Request，可以通过 Issue 提交案例线索。请提供：

- 案件名称；
- 案号；
- 法院；
- 来源链接；
- 简要争议焦点。

维护者会按收录标准核验后决定是否入库。
