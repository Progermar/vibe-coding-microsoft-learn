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

### DRY / Don't Repeat Yourself

Princípio de engenharia que evita duplicar regras, cálculos ou lógica em vários lugares do sistema.

Ideia prática:

```txt
Uma regra importante deve existir em um lugar claro e ser reutilizada por quem precisar dela.
```

Risco quando violado:

```txt
A mesma regra aparece copiada em vários pontos; depois uma alteração corrige um lugar e esquece outro, criando bug ou inconsistência.
```

### SOLID

Conjunto de princípios de organização de software. Para o método atual, a leitura prática é:

```txt
Código dividido em partes menores, com responsabilidades claras, fácil de testar e difícil de quebrar.
```

O objetivo não é decorar a sigla neste momento, mas reconhecer o risco: código gerado ou alterado por IA pode funcionar hoje, mas ficar difícil de manter, testar e evoluir se misturar responsabilidades demais.

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

### 2026-06-11 — CI, CI verde, DevSecOps e curso Microsoft

Novos aprendizados conceituais:

- CI significa Continuous Integration, ou Integração Contínua.
- CI é um robô de validação que executa comandos definidos nos workflows do GitHub Actions.
- CI verde significa que o commit passou nas verificações configuradas.
- CI vermelho significa que alguma verificação configurada falhou.
- CI pendente significa que a validação ainda está rodando.
- CI verde não prova que o sistema está perfeito; prova apenas que passou no que foi configurado para testar.
- Um CI básico pode validar compilação, testes, TypeScript e build.
- Um CI pode detectar erro simples, como aspas esquecida, import quebrado ou falha de build.
- Um CI só detecta erro de regra de negócio se existir teste cobrindo aquela regra.
- DevSecOps adiciona segurança ao fluxo de desenvolvimento, colocando verificações de segurança dentro do pipeline.
- Exemplos de segurança no fluxo: CodeQL, Dependabot, secret scanning, branch protection e security gates.
- O problema não é usar IA para criar software; o problema é usar IA sem processo, testes, revisão, segurança e responsabilidade.
- CI, DevSecOps, revisão de diff, gate humano e handoff ajudam a transformar vibe coding em engenharia assistida por IA.
- O curso da Microsoft entra na camada inicial: ideia, prompt, requisitos, wireframe, protótipo e refinamento com Copilot Agent.
- O método pessoal em construção adiciona a camada de governança: Git, GitHub, commit, push, pull, CI, gate, handoff e DevSecOps.

Frase guia consolidada:

```txt
O problema não é vibe coding. O problema é vibe coding sem processo.
```

Mapa mental:

```txt
Curso Microsoft = aprender a pilotar o Copilot Agent
Git/GitHub = versionar e controlar mudanças
CI = validar automaticamente se algo quebrou
DevSecOps = validar riscos de segurança
Gate/Handoff = manter controle humano, rastreabilidade e continuidade
```

Próximo passo:

Iniciar a primeira unidade do curso Microsoft e registrar os conceitos úteis no repositório.

### 2026-06-11 — SOLID, DRY e paralelo com a refatoração do Dexa

Novos aprendizados:

- O curso alerta que código gerado por IA pode funcionar, mas ainda assim violar boas práticas como SOLID e DRY.
- DRY significa Don't Repeat Yourself: não duplicar regras, cálculos ou lógica em vários lugares.
- SOLID foi entendido de forma prática como: código dividido em partes menores, com responsabilidades claras, fácil de testar e difícil de quebrar.
- A refatoração do Dexa Empresarial é um exemplo real desse aprendizado: reduzir risco estrutural, separar responsabilidades, localizar regras, facilitar testes e diminuir regressão.
- A refatoração não é estética; é engenharia para tornar o sistema mais seguro de manter e evoluir.

Paralelo com o Dexa:

```txt
Antes:
- partes grandes demais;
- regras misturadas;
- busca de dados, cálculo, apresentação e integração próximos demais;
- maior risco de regressão;
- mais dificuldade para testar comportamento.

Depois:
- responsabilidades separadas;
- regras mais localizadas;
- comportamento protegido por testes;
- commits pequenos;
- CI validando;
- gate antes de avançar;
- handoff registrando decisões.
```

Mapa mental de arquitetura:

```txt
SOLID/DRY = qualidade estrutural do código
Testes/CI/gate/commits/handoff = qualidade do processo
```

Frase consolidada:

```txt
A refatoração do Dexa é a aplicação prática dos princípios SOLID/DRY dentro de um fluxo de vibe coding governado: separar responsabilidades, reduzir duplicação, facilitar testes e diminuir risco de regressão.
```

Evolução do papel de engenharia:

```txt
O papel do engenheiro do Dexa foi promovido para Engenheiro de Software e Governança.

Responsabilidade do papel:
- conectar decisões técnicas com governança;
- proteger arquitetura;
- revisar escopo, diff e risco;
- exigir testes quando necessário;
- respeitar CI e gates;
- manter rastreabilidade por commits e handoff;
- transformar vibe coding em engenharia assistida por IA governada.
```
