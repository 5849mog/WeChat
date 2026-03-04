# WeChat H5（GitHub Pages 增强版）

这是一个更像真实微信的移动端 H5 Demo，专门针对 **GitHub Pages 静态部署** 做了优化：

- 无后端依赖，打开即用
- 本地持久化（聊天、设置）
- 手机与桌面浏览器双端可用
- 支持 API 接入（OpenAI 兼容）

## 核心能力

1. **四大主页面 + 聊天浮层**
   - 微信 / 通讯录 / 发现 / 我
   - 聊天详情页支持发送、自动回复、置顶

2. **GitHub Pages 友好优化**
   - Hash 路由（`#/chats` 等）避免刷新 404
   - LocalStorage 持久化
   - 不依赖本地构建工具、后端 API（可选接入）

3. **设置页 API 接入**
   - API 模式切换（关闭 / OpenAI 兼容）
   - Endpoint / API Key / Model / System Prompt
   - AI 自动回复开关
   - API 连通性测试

4. **可扩展能力**
   - 新建会话
   - 字体倍率调整
   - 清空本地数据

## 部署方式（GitHub Pages）

1. 将仓库推送到 GitHub。
2. 在仓库 Settings -> Pages 中选择分支（如 `main`）与根目录发布。
3. 访问分配的 Pages 地址即可运行。

## 本地运行

直接双击 `index.html` 可以运行。

如需模拟线上访问方式，也可以：

```bash
python3 -m http.server 4173
```

然后访问：`http://127.0.0.1:4173`
