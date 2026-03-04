# WeChat H5（精选双对话 + 独立角色引擎）

## 本版核心

- 固定两个精选对话：
  1. **阿泽❤️ 私聊**（你是女性，阿泽是男性情人）
  2. **家庭交流群**（爸爸、妈妈、爷爷、奶奶、外公、外婆、哥哥、你）
- 修复“配置好了却不回复也不报错”：
  - 在线 API 失败会显示错误；
  - 自动回退本地角色引擎，保证不沉默。
- 修复 AI 常见污染输出：
  - 自动清洗 `姓名: 姓名: ...` / 引号前缀等重复头。
- 群聊支持 `@成员` 定向回复：
  - 只要 `@某人`，优先由该成员回复（私信式触发）；
  - 无 @ 时，会有 1~2 名成员自发群发回复。
- 每个成员支持独立 API 配置（Endpoint / Key / Model 覆盖全局）。

## DeepSeek 接入

推荐 endpoint：

- `https://api.deepseek.com/chat/completions`
- 或 `https://api.deepseek.com/v1/chat/completions`

填根地址（如 `https://api.deepseek.com`）会导致 404。
页面中的“修正 Endpoint”可自动补全。

## 参数面板

- provider / api mode
- endpoint / api key / model
- temperature / top_p / max_tokens
- presence_penalty / frequency_penalty
- stop / seed / timeout / stream
- auto reply / font scale / system prompt
- agent-target + 成员独立 endpoint/key/model

## 运行

```bash
python3 -m http.server 4173
```

打开：`http://127.0.0.1:4173/index.html#/chats`
