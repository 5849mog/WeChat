# WeChat H5（GitHub Pages + DeepSeek 增强版）

## 亮点

- 完全静态，适配 GitHub Pages，无需后端。
- 预置更多聊天窗口（工作/家人/兴趣/客户等场景）。
- 真正可用的 API 接入模式（DeepSeek / OpenAI / 自定义兼容接口）。
- 提供完整参数面板：
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
- 聊天、设置本地持久化（LocalStorage）。

## DeepSeek 接入建议

推荐 endpoint：

- `https://api.deepseek.com/chat/completions`
- 或 `https://api.deepseek.com/v1/chat/completions`

如果只填根地址（例如 `https://api.deepseek.com`）通常会 404。
项目内置「修正 Endpoint」按钮可自动补全。

常用模型：

- `deepseek-chat`
- `deepseek-reasoner`

## 部署

1. 推送到 GitHub。
2. 在仓库 Settings -> Pages 启用分支发布。
3. 打开 Pages 链接即可。

## 本地运行

```bash
python3 -m http.server 4173
```

打开 `http://127.0.0.1:4173/index.html#/chats`
