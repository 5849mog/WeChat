# WeChat H5（精选双对话 + DeepSeek 完整接入）

## 本版重点

- 只保留两个精选对话：
  1. **林妍❤️（私聊）**：亲密关系场景。
  2. **家庭交流群（群聊）**：包含爸爸、妈妈、爷爷、奶奶、外公、外婆、哥哥、你本人。
- 修复“配置好了但不回复也不报错”：
  - API 失败会提示具体原因；
  - 并自动回退本地角色引擎，**不会沉默**。
- 支持群聊 `@成员`（如 `@妈妈`、`@哥哥`），被 @ 成员优先回复。

## DeepSeek 正确接入

推荐 endpoint：

- `https://api.deepseek.com/chat/completions`
- 或 `https://api.deepseek.com/v1/chat/completions`

如果填成根地址（例如 `https://api.deepseek.com`）常见 404。
项目里有“修正 Endpoint”按钮会自动补全。

## 参数面板（完整）

- provider
- api mode
- endpoint
- api key
- model
- temperature
- top_p
- max_tokens
- presence_penalty
- frequency_penalty
- stop
- seed
- timeout
- stream
- auto reply
- system prompt
- font scale

## 部署 / 运行

### GitHub Pages
1. 推送仓库到 GitHub。
2. Settings -> Pages 打开分支发布。
3. 访问 Pages 地址。

### 本地
```bash
python3 -m http.server 4173
```
打开：`http://127.0.0.1:4173/index.html#/chats`
