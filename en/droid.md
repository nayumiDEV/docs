# Using Agent Router with Droid CLI


## Install Droid Cli

::: code-group

```bash [macos/Linux]
curl -fsSL https://app.factory.ai/cli | sh
```

```bash [Windows]
irm https://app.factory.ai/cli/windows | iex

```


:::
## Configure Model

Edit `~/.factory/config.json`, change the content to the following, remember to replace YOUR_AGENT_ROUTER_KEY with your AgentRouter Key

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
}
```



## Launch Directly

After configuration, type `droid` in the command line, and in the interface that appears type `/model`, and select `agentrouter-gpt5` in Custom Model to start using
