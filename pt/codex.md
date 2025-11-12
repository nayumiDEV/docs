# Usando Agent Router com Codex

## Instalar Codex

::: code-group

```bash [pnpm]
pnpm install -g @openai/codex
```

```bash [npm]
npm install -g @openai/codex
```

```bash [yarn]
yarn global add @openai/codex
```

:::

## Configurar Variáveis de Ambiente

1. Visite https://agentrouter.org/console/token para obter sua API Key
2. Defina a variável de ambiente do sistema com o nome `AGENT_ROUTER_TOKEN` e o valor que você acabou de obter ([Tutorial de Configuração de Variável de Ambiente](https://www.java.com/pt-BR/download/help/path.html))
3. Crie o arquivo `~/.codex/config.toml` e adicione a seguinte configuração:

```toml
model = "gpt-5"
model_provider = "openai-chat-completions"
preferred_auth_method = "apikey"


[model_providers.openai-chat-completions]
name = "OpenAI using Chat Completions"
base_url = "https://agentrouter.org/v1"
env_key = "AGENT_ROUTER_TOKEN"
wire_api = "chat"
query_params = {}
stream_idle_timeout_ms = 300000

```

4. Crie o arquivo `~/.codex/auth.json` e adicione o seguinte código:

```json
{
 "OPENAI_API_KEY":"Substitua isso pela sua API KEY"
}
```

## Iniciar Diretamente

Após configurar as variáveis de ambiente, use seu terminal para abrir o diretório do projeto com o qual deseja trabalhar e execute o seguinte comando para iniciar o Codex:

```bash
cd meu-projeto

codex
```


## Usando Codex no VSCode


1. Siga as instruções acima para instalar o Codex e configurar variáveis de ambiente e arquivos de configuração.

2. Abra o VSCode e instale a [extensão Codex](https://marketplace.visualstudio.com/items?itemName=openai.chatgpt).

3. Vá para configurações e clique no ícone no canto superior direito para alternar para o modo de configuração JSON

![](../img/codex-config.png)

4. Adicione os seguintes itens de configuração:


```json
"chatgpt.apiBase": "https://agentrouter.org/v1",
"chatgpt.config": {
    "pepreferred_auth_method": "api_key",
    "model_provider": "openai-chat-completions"
}
```

![](../img/codex-config2.png)


5. Clique no ícone do Codex para começar a usar...
