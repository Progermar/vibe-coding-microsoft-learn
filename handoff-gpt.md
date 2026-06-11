# HANDOFF-GPT

## Objetivo do repositório

Este repositório é um caderno técnico e laboratório prático para acompanhar o curso Introduction to Vibe Coding da Microsoft Learn.

## Estado atual

- Repositório criado no GitHub.
- Repositório clonado localmente.
- Branch atual: main.
- Working tree: clean.
- Primeiro arquivo existente: README.md.
- Arquivo de metodologia criado: HANDOFF-GPT.md.

## Metodologia em teste

Este repositório será usado para testar um fluxo de desenvolvimento assistido por IA com:

- contexto claro;
- prompts versionados;
- handoff entre sessões;
- revisão humana;
- commits pequenos;
- GitHub como fonte da verdade.

## Vocabulário técnico inicial

### Vibe Coding

Desenvolver software guiando a IA por intenção, contexto e feedback, em vez de escrever cada linha manualmente.

### Prompt

A instrução dada para a IA.

### Contexto

Informações que a IA precisa para responder bem, como objetivo, stack, estrutura do projeto, regras, arquivos relevantes e decisões anteriores.

### Iteração

Ciclo de melhoria: pedir, testar, corrigir, ajustar e validar novamente.

### Agent / Agente

IA que consegue executar tarefas usando ferramentas, como editar arquivos, rodar comandos, testar, criar commits ou abrir pull requests.

### Copilot Agent

Modo do GitHub Copilot em que ele executa uma tarefa dentro do projeto, não apenas sugere código.

### Handoff

Passagem organizada de contexto de uma sessão ou agente para outra.

### Source of Truth / Fonte da verdade

Local oficial onde está o estado confiável do projeto.

Neste repositório, a fonte da verdade será:

- GitHub;
- arquivos versionados;
- histórico de commits;
- handoffs registrados.

### Spec / Especificação

Documento curto que explica exatamente o que deve ser feito, por quê, onde mexer e como validar.

### Requirements / Requisitos

O que o produto, protótipo ou tarefa precisa fazer.

### Wireframe

Rascunho visual simples de uma tela antes do design final.

### Prototype / Protótipo

Versão inicial funcional ou visual criada para testar uma ideia rapidamente.

### Validation / Validação

Conferência para saber se o que foi feito realmente funciona.

Pode incluir:

- revisão humana;
- testes;
- execução local;
- comparação com requisitos;
- CI.

### CI / Continuous Integration

Pipeline automático que roda testes, build e verificações quando o código é enviado para o GitHub.

### Guardrail

Regra de proteção para impedir que a IA faça alterações perigosas, fora do escopo ou sem validação.

### Refactor / Refatoração

Melhorar a estrutura do código sem mudar o comportamento esperado.

### Regression / Regressão

Quando algo que funcionava para de funcionar depois de uma alteração.

### Diff

Diferença entre o código ou arquivo antes e depois de uma alteração.

### Commit

Registro de uma mudança no Git.

### Push

Envio dos commits locais para o GitHub.

### Pull

Atualização do repositório local com alterações vindas do GitHub.

### Branch

Linha de trabalho dentro do Git.

### Main

Branch principal do projeto.

### Origin/main

Branch principal que está no GitHub.

### Merge

Juntar uma branch ou subtarefa aprovada na branch principal.

### Pull Request / PR

Pedido para revisar e juntar uma alteração ao código principal.

### Gate

Ponto de parada obrigatório antes de avançar.

Exemplo:

- revisão do GPT engenheiro;
- aprovação humana;
- CI verde;
- testes passando;
- diff revisado.

## Fluxo mental principal

Prompt → Contexto → Spec → Agent → Iteração → Validação → Diff → Commit → Push → CI → Gate → Handoff

## Frase guia

Eu uso vibe coding com processo: primeiro dou contexto, gero uma spec, deixo o agente implementar, valido por testes e CI, reviso o diff e só então avanço.

## Próximo passo

Criar a estrutura inicial de pastas e arquivos para organizar o estudo do curso.

---

## Registro da sessão

### 2026-06-11 — Fundamentos Git, GitHub e handoff assistido por IA

Aprendizados consolidados:

- README.md apresenta o repositório.
- .gitignore define arquivos que o Git deve ignorar.
- main é a branch principal local.
- origin/main é a branch principal no GitHub.
- git status mostra o estado do repositório.
- working tree clean significa que não há alterações pendentes.
- untracked significa arquivo novo ainda não rastreado.
- git add prepara o arquivo para commit.
- staged significa preparado para commit.
- git commit cria o registro oficial da mudança.
- -m define a mensagem do commit.
- SHA identifica um commit.
- git push envia commits locais para o GitHub.
- git pull traz commits do GitHub para o computador.
- merge junta uma branch ou subtarefa aprovada na main.
- gate é um ponto de aprovação antes de avançar.

Fluxo local praticado:

editar arquivo → git add → git commit → git push

Fluxo remoto pelo GPT:

GPT edita no GitHub → commit nasce no remoto → usuário roda git pull → computador atualizado

### 2026-06-11 — Consolidação: fetch, pull e pedido de atualização remota

Novos aprendizados:

- `git fetch` consulta o GitHub, baixa as referências novas e atualiza `origin/main`, mas não altera os arquivos locais.
- Depois do `git fetch`, o `git status` consegue mostrar se a branch local está atrás de `origin/main`.
- `git pull` baixa e aplica as mudanças remotas nos arquivos locais.
- Quando o GPT edita diretamente no GitHub, o commit nasce no remoto; depois o usuário pode usar `git fetch` para inspecionar e `git pull` para trazer a alteração.
- O pedido operacional correto para o agente é: "Atualize o HANDOFF-GPT.md com os aprendizados desta etapa. Faça commit direto no GitHub e me retorne o SHA para eu puxar localmente com git pull."

Fluxo didático aprendido:

```txt
git status → git fetch → git status → git pull → git status
```

Interpretação:

```txt
git fetch = descobrir e baixar referências remotas
git pull = aplicar as mudanças remotas no trabalho local
```

Próximo teste:

Rodar `git fetch`, conferir o avanço de `origin/main`, depois rodar `git pull` e finalizar com `git status` limpo.
