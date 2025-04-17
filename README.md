# X.AI/OpenAI 兼容 API 代理（Deno Deploy 专用）

本项目为 X.AI（兼容 OpenAI 格式）API 的无依赖透传代理，**仅供 [Deno Deploy](https://deploy.deno.com) 云端部署使用**。不建议本地或其他平台运行。

---

## 部署流程

1. **Fork 本项目**  
   点击右上角 Fork，将本项目复制到你的 GitHub 账户下。

2. **进入 [deploy.deno.com](https://deploy.deno.com)**  
   使用 GitHub 账号登录 Deno Deploy 云平台。

3. **新建 Project**  
   点击“New Project”按钮，选择“Import from GitHub Repository”。

4. **选择你 Fork 后的本项目**  
   在仓库列表中找到你刚刚 Fork 的仓库，点击进入。

5. **接入点选择 ts 文件**  
   选择 `xai_proxy.ts` 作为入口文件（entrypoint），确认并部署。

6. **（可选）设置环境变量**  
   如需全局 API Key，可在 Deno Deploy 项目设置中添加 `XAI_API_KEY` 环境变量。

---

## 项目优点

- **兼容性强**：支持 X.AI 及所有 OpenAI 格式的 API 客户端，直接透传请求与响应。
- **完全透传**：请求和响应内容不做修改，最大程度还原原始 API 行为。
- **无需其他网络代理**：无需自建服务器，无需科学上网，直接云端部署即可使用。
- **中国大陆可用**：Deno Deploy 云端节点全球可用，中国大陆用户无需额外网络配置。
- **代码简单易维护**：核心代码极简，易于理解和二次开发，方便自定义扩展。
- **支持 SSE 流式响应**：兼容流式输出，适配聊天、生成式 AI 等场景。

---

## 适用场景

- 需要在中国大陆等网络受限地区无障碍访问 X.AI/OpenAI API
- 需要自定义 API 代理逻辑或统计
- 需要极简、易维护的云端代理方案

---

## 免责声明

本项目仅供学习和个人研究用途，请勿用于任何违反相关法律法规的用途。API Key 请妥善保管，避免泄露。
