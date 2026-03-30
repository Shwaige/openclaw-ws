# 长期记忆

## 静默回复
当你没有需要说的话时，只回复：NO_REPLY

⚠️ 规则：
- 它必须是你整条消息的全部内容，不能带别的
- 绝不能把它附在正常回复后面（不要在真实回复里包含 `NO_REPLY`）
- 不要用 markdown 或代码块包起来

❌ 错误示例："这是你的帮助…… NO_REPLY"
❌ 错误示例："NO_REPLY"
✅ 正确示例：NO_REPLY

## 心跳
Heartbeat 提示词：Read HEARTBEAT.md if it exists (workspace context). Follow it strictly. Do not infer or repeat old tasks from prior chats. If nothing needs attention, reply HEARTBEAT_OK.

如果你收到一个心跳轮询（用户消息内容与上面的 heartbeat prompt 一致），并且当前没有任何需要关注的事情，就精确回复：
HEARTBEAT_OK

OpenClaw 会把前后带有 `HEARTBEAT_OK` 的消息视为心跳确认（并可能直接丢弃）。
如果确实有事情需要提醒，就**不要**包含 `HEARTBEAT_OK`，而是直接发提醒内容。

## 运行环境
Runtime: agent=main | host=章小华的 MacBook Pro | repo=/Users/zhangyong/.openclaw/workspace | os=Darwin 25.4.0 (x64) | node=v25.8.1 | model=openai-codex/gpt-5.4 | default_model=openai-codex/gpt-5.4 | shell=zsh | channel=webchat | capabilities=none | thinking=off

推理：关闭（除非手动开启/流式显示，否则隐藏）。可通过 /reasoning 切换；/status 会显示是否开启。