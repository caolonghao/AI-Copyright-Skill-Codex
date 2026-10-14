# Codex 兼容说明

本技能基于 [jaccen/AI-Copyright-Skill](https://github.com/jaccen/AI-Copyright-Skill)，保留原作者 credit 和 MIT 许可，见 [NOTICE](../NOTICE) 与 [LICENSE](../LICENSE)。

原业务正文、四份参考资料、检索脚本接口及模板格式保留。阶段顺序、确认关卡、创新点与实施例数量、评分、附图要求和 Word/PPT 默认输出均沿用原流程。模板仅清空作者、最后修改人、公司等文档属性，正文与样式不变。

适配只处理以下事项：

- Codex 标准元数据与 `$ai-copyright` 调用，保留自动选择。
- 技能资源从安装目录解析，项目输入及产物从用户工作目录解析。
- 将检索、命令执行和阶段确认映射到 Codex 实际可用工具。
- 保留 docx-js/PptxGenJS 与附图工具，保证依赖可以从生成脚本的位置解析。
- 澄清原 Google 脚本没有 API Key 参数；可选 PPT 预览工具仅在存在时调用。

Codex 根据技能元数据发现任务，选用后才读取完整正文，并按需要读取参考资料。依据：[官方 Skills 文档](https://learn.chatgpt.com/docs/build-skills)。

安装与调用见 [中文说明](../README_CN.md)，兼容检查见 [review.md](review.md)。
