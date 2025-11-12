# Utiliser Agent Router avec Droid CLI


## Installer Droid Cli

::: code-group

```bash [macos/Linux]
curl -fsSL https://app.factory.ai/cli | sh
```

```bash [Windows]
irm https://app.factory.ai/cli/windows | iex

```


:::
## Configurer le Modèle

Modifiez `~/.factory/config.json`, changez le contenu comme suit, n'oubliez pas de remplacer YOUR_AGENT_ROUTER_KEY par votre AgentRouter Key

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



## Lancer Directement

Après la configuration, tapez `droid` dans la ligne de commande, et dans l'interface qui apparaît tapez `/model`, et sélectionnez `agentrouter-gpt5` dans Custom Model pour commencer à utiliser
