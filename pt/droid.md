# Usando Agent Router com Droid CLI


## Instalar Droid Cli

::: code-group

```bash [macos/Linux]
curl -fsSL https://app.factory.ai/cli | sh
```

```bash [Windows]
irm https://app.factory.ai/cli/windows | iex

```


:::
## Configurar Modelo

Edite `~/.factory/config.json`, altere o conteúdo para o seguinte, lembre-se de substituir YOUR_AGENT_ROUTER_KEY pela sua AgentRouter Key

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



## Iniciar Diretamente

Após a configuração, digite `droid` na linha de comando e na interface que aparecer digite `/model`, e selecione `agentrouter-gpt5` em Custom Model para começar a usar
