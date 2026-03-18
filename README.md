# AutoHook

SKILL 自审计钩子系统 - 为 SKILL 注入强制自审计功能，确保执行质量。

## 功能

- **钩子注入**：自动为指定 SKILL.md 注入自审计钩子
- **钩子撤销**：删除已注入的钩子，恢复 SKILL 原样
- **跨平台支持**：适配 Claude Code、OpenAI Codex CLI、OpenClaw 三大智能体
- **路径自动适配**：自动识别 Linux / macOS / Windows 路径

## 触发词

### 注入触发词
- 「检查 XX skill 有没有偷懒」
- 「审计 XX skill」
- 「给 XX skill 加钩子」
- 「验证 XX skill 执行质量」

### 撤销触发词
- 「停止检查 XX skill」
- 「取消 hook」
- 「删除钩子」
- 「还原 XX skill」

## 文件说明

| 文件 | 说明 |
|------|------|
| `SKILL.md` | 主技能定义文件 |
| `hook.md` | 自审计钩子模板（可注入到任意 SKILL 末尾） |
| `skill-audit-hook.txt` | 钩子注入的源内容 |
| `README.md` | 项目说明 |

## 工作原理

1. 定位目标 SKILL.md 文件
2. 读取 `skill-audit-hook.txt` 完整内容
3. 检测 SKILL 是否已有 autohook
4. 若无，则追加钩子内容到 SKILL.md 末尾
5. 验证并输出结果

## 许可证

MIT
