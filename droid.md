# 在 Droid CLI 中使用 Agent Router


## 安装 Droid Cli

::: code-group

```bash [macos/Linux]
curl -fsSL https://app.factory.ai/cli | sh
```

```bash [Windows]
irm https://app.factory.ai/cli/windows | iex

```


:::
## 配置模型

编辑 `~/.factory/config.json` , 将内容修改为如下内容，记得将 YOUR_AGENT_ROUTER_KEY 替换为你的 AgentRouter Key

```json
{
    "custom_models": [
        {
            "model_display_name": "agentrouter-gpt5",
            "model": "gpt-5",
            "base_url": "https://agentrouter.org/v1",
            "api_key": "YOUR_AGENT_ROUTER_KEY",
            "provider": "generic-chat-completion-api",
            "max_tokens": 1280000
        }
    ]

```



## 直接启动使用

配置好后，命令行输入 `droid` ，并在弹出的界面输入 `/model`,并选择 Custom Model 中的 `agentrouter-gpt5` 即可