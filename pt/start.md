# Usando Agent Router com Claude Code

## Instalar Claude Code

::: code-group

```bash [pnpm]
pnpm install -g @anthropic-ai/claude-code
```

```bash [npm]
npm install -g @anthropic-ai/claude-code
```

```bash [yarn]
yarn global add @anthropic-ai/claude-code
```

:::

## Configurar Variáveis de Ambiente

Digite os seguintes comandos no seu terminal para definir as variáveis de ambiente para usar a API Anthropic do AgentRouter:

::: code-group

```bash [Linux/macOS]
export ANTHROPIC_BASE_URL=https://agentrouter.org/

export ANTHROPIC_AUTH_TOKEN=sk-xxx
export ANTHROPIC_API_KEY=sk-xxx
```

```powershell [Windows PowerShell]
$env:ANTHROPIC_BASE_URL="https://agentrouter.org/"

$env:ANTHROPIC_AUTH_TOKEN="sk-xxx"
$env:ANTHROPIC_API_KEY="sk-xxx"
```

```cmd [Windows CMD]
set ANTHROPIC_BASE_URL=https://agentrouter.org/

set ANTHROPIC_AUTH_TOKEN=sk-xxx
set ANTHROPIC_API_KEY=sk-xxx
```

:::

> [!IMPORTANT]
> Certifique-se de substituir sk-xxx pelo Token fornecido pelo AgentRouter. Você pode obter sua API Key no [Console AgentRouter](https://agentrouter.org/console/token).


## Iniciar Diretamente

Após configurar as variáveis de ambiente, use seu terminal para abrir o diretório do projeto com o qual deseja trabalhar e execute o seguinte comando para iniciar o Claude Code:

::: code-group

```bash [Linux/macOS]
cd meu-projeto

claude
```

```powershell [Windows PowerShell]
cd meu-projeto

claude
```

```cmd [Windows CMD]
cd meu-projeto

claude
```

:::

## Seleção de Modelo

Você pode controlar a escolha do modelo do Claude Code usando variáveis de ambiente:

| Variável | Descrição |
| -------- | ----------- |
| ANTHROPIC_MODEL | Modelo principal para Claude Code. Aceita um alias de modelo (ex: sonnet, haiku) ou um nome completo de modelo. |
| ANTHROPIC_SMALL_FAST_MODEL | Modelo rápido e de baixa latência para operações leves/em segundo plano. Obsoleto e mantido apenas para compatibilidade. |

Nomes de modelos recomendados por exemplo:

`claude-sonnet-4-5-20250929` `claude-sonnet-4-5-20250514` `claude-haiku-4-5-20251001` `claude-3-5-haiku-20241022`


::: code-group

```bash [Linux/macOS]
export ANTHROPIC_MODEL=claude-sonnet-4-5-20250929
export ANTHROPIC_SMALL_FAST_MODEL=claude-3-5-haiku-20241022

claude
```

```powershell [Windows PowerShell]
$env:ANTHROPIC_MODEL = "claude-sonnet-4-5-20250929"
$env:ANTHROPIC_SMALL_FAST_MODEL = "claude-3-5-haiku-20241022"

claude
```

```bash [Windows CMD]
set ANTHROPIC_MODEL=claude-sonnet-4-5-20250929
set ANTHROPIC_SMALL_FAST_MODEL=claude-3-5-haiku-20241022

claude
```

:::


> [!NOTE]
> ANTHROPIC_SMALL_FAST_MODEL está obsoleto. Migre quando possível para os padrões Haiku recomendados. Até a migração, ainda será respeitado para operações rápidas/em segundo plano legadas. ANTHROPIC_MODEL permanece o controle principal para codificação interativa e tarefas gerais.
