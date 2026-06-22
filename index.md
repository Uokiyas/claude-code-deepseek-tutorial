# Claude Code + DeepSeek 挂载教程 🎬

> 把 DeepSeek 挂到 Obsidian 上 · 第一期
> 本期目标：让 Claude Code 能通过 CC-Switch 调用 DeepSeek 模型

---

## 目录

- [第一步：安装 Node.js](#第一步安装-nodejs)
- [第二步：安装 Claude Code](#第二步安装-claude-code)
- [第三步：验证安装](#第三步验证安装)
- [第四步：下载 CC-Switch](#第四步下载-cc-switch)
- [第五步：获取 DeepSeek API Key](#第五步获取-deepseek-api-key)
- [第六步：把 API Key 关联到 CC-Switch](#第六步把-api-key-关联到-cc-switch)
- [第七步：测试](#第七步测试)

---

## 第一步：安装 Node.js

Claude Code 依赖 Node.js 环境，需要先装它。

**下载地址：** [https://nodejs.org/en/download/](https://nodejs.org/en/download/)

安装完成后，打开终端验证：

```bash
node --version
npm --version
```

两条命令都应该返回版本号。

---

## 第二步：安装 Claude Code

在终端执行：

```bash
sudo npm install -g @anthropic-ai/claude-code
```

> 加 `sudo` 是因为全局安装需要写入系统目录。如果提示密码，输入电脑的开机密码即可。

---

## 第三步：验证安装

```bash
claude --version
```

如果显示了版本号（比如 `0.x.x`），说明 Claude Code 安装成功。

---

## 第四步：下载 CC-Switch

CC-Switch 是一个模型网关层，让 Claude Code 可以调用非 Claude 的模型（比如 DeepSeek）。

**下载地址：** [https://ccswitch.io/zh/](https://ccswitch.io/zh/)

> 下载后解压到一个固定的目录，后面配置要用。

---

## 第五步：获取 DeepSeek API Key

1. 打开 DeepSeek 开发者平台 → 注册 / 登录
   **网址：** [https://platform.deepseek.com/api_keys](https://platform.deepseek.com/api_keys)
2. 进入 API Keys 页面 → 创建一个新的 Key
3. 复制保存好（关掉页面就看不到了）

### 为什么要选 DeepSeek？

DeepSeek 的 API 价格很低，能力也够用。一般充 10 块钱可以用很久很久。如果刚开始想简单试试，先充一点点就行。

---

## 第六步：把 API Key 关联到 CC-Switch

1. 启动 CC-Switch（双击或终端运行）
2. 在配置界面里：
   - 添加一个新的模型提供商 → 选 DeepSeek
   - 粘贴刚才复制的 API Key
   - 选择模型（如 DeepSeek V4 Pro）
3. 保存配置

---

## 第七步：测试

确认 CC-Switch 已启动，然后终端运行 `claude` 启动 Claude Code，随便问一个问题（比如"用中文说一句话"）。

- 如果能正常回复 → ✅ 全部通了
- 如果卡住或报错 → 检查 CC-Switch 里的 API Key 和模型配置

> 注意：直接运行 `claude` 只是进入了界面，**不能**验证 DeepSeek API 是否生效。必须完成 CC-Switch 配置后再测试。

---

## 下期预告

第二期内容：
- 安装 Obsidian（如果还没有）
- 安装 Claudian 插件
- 配置 Claudian 连接 DeepSeek
- 演示：AI 自动分析笔记、建立知识关联

---

> 本教程由 [Claudian](https://github.com/anthropics/claude-code) 整理生成
