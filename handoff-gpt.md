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

### 2026-06-11 — Processo de vibe coding, brownfield, wireframe e governança contínua

Unidade estudada:

```txt
Examine o processo de codificação Vibe
```

Aprendizados principais:

- O processo de vibe coding pode ser entendido em três fases: prever/planejar, desenvolver um protótipo inicial e evoluir recursos de forma iterativa.
- Greenfield é projeto criado do zero, com liberdade maior para definir arquitetura, stack, pastas, padrões e fluxo desde o início.
- Brownfield é projeto já existente, com código, regras, banco, usuários, histórico e risco de regressão.
- O Dexa Empresarial é um projeto brownfield; portanto, vibe coding nele deve ser aplicado com escopo pequeno, cuidado arquitetural, testes, CI, gate e handoff.
- A fase iterativa do vibe coding pode ser aplicada em projetos brownfield mesmo que o projeto não tenha nascido com vibe coding.
- Em brownfield, vibe coding não significa deixar a IA reconstruir tudo; significa usar IA para evoluir o sistema em ciclos curtos, seguros e revisáveis.

Paralelo prático com o Dexa:

```txt
Projeto brownfield:
- não começar por liberdade criativa;
- não pedir "refaça tudo";
- não deixar executor decidir arquitetura sozinho.

Fluxo correto:
- consultar o Engenheiro de Software e Governança;
- transformar a demanda em spec pequena;
- enviar ao agente executor;
- revisar diff;
- validar comportamento;
- rodar testes/CI;
- passar pelo gate;
- registrar handoff.
```

Separação de papéis consolidada:

```txt
Claude / Codex = agente executor
Engenheiro de Software e Governança = direção, revisão, risco e decisão técnica
Usuário = dono do produto e aprovador final
```

Regra consolidada:

```txt
Em projeto brownfield, o agente executor não deve decidir arquitetura sozinho. Ele executa uma spec validada pelo Engenheiro de Software e Governança.
```

Aprendizado sobre wireframe:

- Foi identificado um gap no processo anterior: telas foram refinadas por tentativa prática, sem wireframe prévio.
- Esse caminho funciona, mas aumenta retrabalho, conversa, risco de interpretação errada e inconsistência visual.
- Wireframe deve entrar como rascunho visual antes da implementação.
- Para telas existentes, o fluxo ideal é: print da tela atual → diagnóstico UX → mini-wireframe de melhoria → spec → implementação.
- Para telas novas, o fluxo ideal é: mini-wireframe → spec → implementação.

Regra nova para UX no Dexa:

```txt
Mudança visual relevante no Dexa
→ mini-wireframe
→ spec
→ implementação
→ diff
→ testes/validação
→ CI
→ gate
```

Frase consolidada:

```txt
Wireframe = gate visual antes da implementação.
```

Aprendizado sobre documentação e qualidade contínua:

- A IA no vibe coding não deve ser usada apenas para gerar código.
- A IA também pode apoiar documentação automatizada, comentários relevantes, wikis, revisão de qualidade, identificação de bugs, análise de segurança, refatoração assistida e análise de performance.
- Comentários de código devem explicar lógica complexa e decisões importantes, não repetir o óbvio.
- Wikis e documentação devem preservar conhecimento do projeto: setup, testes, arquitetura, motor de relatórios, CR/CP, fluxo de caixa e guias de operação.
- Revisão automatizada pode ajudar a localizar bugs, vulnerabilidades, gargalos de performance e violações de padrões.
- A melhoria contínua do código passa a fazer parte do processo, não uma etapa isolada.

Paralelo com governança:

```txt
IA como executor = gera ou altera código.
IA como apoio de governança = documenta, revisa, audita, compara, explica, refatora e ajuda a preservar conhecimento.
```

Frases consolidadas:

```txt
A IA no vibe coding não deve ser usada apenas para gerar código. Ela também deve atuar como apoio à documentação, revisão de qualidade, refatoração, análise de segurança, performance e preservação de conhecimento do projeto.
```

```txt
No Dexa, documentação, comentários relevantes, wikis, revisão automatizada, refatoração assistida e análise de performance passam a fazer parte da governança do desenvolvimento assistido por IA.
```

Síntese da unidade:

```txt
O curso ensina que vibe coding é um processo iterativo. No método do usuário, esse processo foi elevado para engenharia assistida por IA governada: contexto, spec, executor, diff, testes, CI, gate, wireframe quando houver UX e handoff como memória operacional.
```
1. Documentação
- explicar funções importantes;
- documentar APIs;
- criar exemplos de uso;
- manter handoffs e guias técnicos.

2. Comentários de código
- comentar apenas lógica complexa;
- explicar decisões difíceis;
- evitar comentário óbvio.

3. Wiki / Base de conhecimento
- guias de setup;
- como rodar testes;
- como funciona o motor de relatórios;
- como funciona CR/CP/Fluxo de Caixa.

4. Qualidade contínua
- revisão automatizada;
- identificar bugs potenciais;
- localizar vulnerabilidades;
- reforçar padrões;
- apoiar refatoração;
- analisar performance.

Regra permanente:
Sempre traçar paralelo entre o conceito estudado no curso e o Dexa Empresarial, pois o Dexa é o laboratório real de aplicação da governança de vibe coding.

