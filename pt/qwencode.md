# Usando Agent Router com Qwen Code


## Instalar Qwen Code

::: code-group

```bash [pnpm]
pnpm install -g @qwen-code/qwen-code
```

```bash [npm]
npm install -g @qwen-code/qwen-code
```

```bash [yarn]
yarn global add @qwen-code/qwen-code
```

:::

## Configurar Variáveis de Ambiente

Digite os seguintes comandos no seu terminal para definir as variáveis de ambiente ([Tutorial de Configuração de Variável de Ambiente](https://www.java.com/pt-BR/download/help/path.html)) para usar a API OpenAI do AgentRouter:

::: code-group

```bash [Linux/macOS]
export OPENAI_API_KEY="sk-xxx"
export OPENAI_BASE_URL="https://agentrouter.org/v1"
export OPENAI_MODEL="gpt-5"
```

```powershell [Windows PowerShell]
$env:OPENAI_API_KEY="sk-xxx"
$env:OPENAI_BASE_URL="https://agentrouter.org/v1"
$env:OPENAI_MODEL="gpt-5"
```

```bash [Windows CMD]
set OPENAI_API_KEY="sk-xxx"
set OPENAI_BASE_URL="https://agentrouter.org/v1"
set OPENAI_MODEL="gpt-5"
```

:::

> [!IMPORTANT]
> Certifique-se de substituir sk-xxx pelo Token fornecido pelo AgentRouter. Você pode obter sua API Key no [Console AgentRouter](https://agentrouter.org/console/token).


## Iniciar Diretamente

Após configurar as variáveis de ambiente, use seu terminal para abrir o diretório do projeto com o qual deseja trabalhar e execute o seguinte comando para iniciar o Qwen Code:

```bash
cd meu-projeto

qwen
```

::: tip
Você pode adicionar a configuração de variável de ambiente ao seu arquivo de configuração do shell para evitar configuração manual toda vez:

::: code-group

```bash [Linux/macOS]
export OPENAI_API_KEY="sk-xxx"
export OPENAI_BASE_URL="https://agentrouter.org/v1"
export OPENAI_MODEL="gpt-5"
```

```powershell [Windows PowerShell]
$env:OPENAI_API_KEY="sk-xxx"
$env:OPENAI_BASE_URL="https://agentrouter.org/v1"
$env:OPENAI_MODEL="gpt-5"
```

```bash [Windows CMD]
set OPENAI_API_KEY="sk-xxx"
set OPENAI_BASE_URL="https://agentrouter.org/v1"
set OPENAI_MODEL="gpt-5"
```

:::
