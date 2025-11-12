# Usando Agent Router con Droid CLI


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

Edite `~/.factory/config.json`, cambie el contenido al siguiente, recuerde reemplazar YOUR_AGENT_ROUTER_KEY con su AgentRouter Key

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



## Iniciar Directamente

Después de la configuración, escriba `droid` en la línea de comandos, y en la interfaz que aparece escriba `/model`, y seleccione `agentrouter-gpt5` en Custom Model para comenzar a usar
