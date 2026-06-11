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