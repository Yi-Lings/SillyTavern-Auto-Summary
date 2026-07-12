# SillyTavern 全自动总结 V1.0

基于 JS-Slash-Runner（酒馆助手）的 SillyTavern 自动对话总结脚本。自动将聊天记录总结为结构化摘要并存入世界书，支持自定义 API、多级权重评分、暗色主题。

## 功能

- **自动触发总结** — 当未总结消息数达到阈值时自动触发，无需手动操作
- **自定义 API** — 支持任意 OpenAI 兼容的 API，在弹窗中独立配置 URL / Key / 模型，支持测试API通断
- **世界书集成** — 总结结果自动写入当前角色的主世界书
- **双模式** — 小总结（默认10 /次）与大总结（默认30 条/次），按需修改
- **权重评分** — 每条总结附带 10 维度权重评分，支持按权重筛选查看
- **暗色主题** — 内置多色主题，根据 accent 颜色自动切换明暗
- **服务端代理** — 通过 SillyTavern 后端代理 API 请求，彻底规避浏览器 CORS 限制
- **手动 / 自动** — 支持手动单次总结和全自动批量总结
- **导入包** — 附带 JS-Slash-Runner 导入包 JSON，一键导入

## 环境要求

- [SillyTavern](https://github.com/SillyTavern/SillyTavern) v1.12.13+
- [JS-Slash-Runner (酒馆助手)](https://github.com/N0VI028/JS-Slash-Runner) 扩展
- 一个 OpenAI 兼容的 API (或通过 SillyTavern 的 API 连接)

## 安装说明

### 方式一：导入包（推荐）

1. 在 SillyTavern 中打开酒馆助手
2. 点击"导入" → 选择 `SillyTavern全自动总结V1.0_导入包.json`
3. 刷新页面

### 方式二：手动添加

将 `SillyTavern全自动总结V1.0.js` 放入 JS-Slash-Runner 脚本目录，或作为用户脚本加载。

## 使用说明

1. 点击 SillyTavern 扩展菜单中的"全自动总结"入口
2. 在弹窗中配置 API URL、API Key
3. 点击"加载模型"选择模型
4. 点击"测试连接"验证配置
5. 点击"手动总结"或开启"自动总结"

### API 配置

- **API 基础 URL**: 你的 API 端点 (如 `https://api.openai.com/v1`)
- **API 密钥**: 你的 API Key
- 配置存储在浏览器 localStorage，私密安全

### 主题定制

点击色块按钮切换主题色，或使用颜色选择器自定义。深色 accent 自动切换暗色主题。

## 文件说明

| 文件 | 说明 |
|------|------|
| `SillyTavern全自动总结V1.0.js` | 主脚本 (UserScript 格式) |
| `SillyTavern全自动总结V1.0_导入包.json` | JS-Slash-Runner 导入包 |

## License

MIT
