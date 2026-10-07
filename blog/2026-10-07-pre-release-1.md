---
title: "Pré-release 1 - 07/10/2026"
authors: "Mendezalv"
tags: [pre-release-1]
date: 2026-10-07
---

## Conte como tem sido o ritmo de trabalho da sua equipe nesta fase de preparação para a primeira entrega.

Nesta fase de reta final para a Release 1, o ritmo de trabalho da equipe se intensificou consideravelmente. Mantivemos o ciclo de sprints semanais com reuniões de planejamento e retrospectiva, mas à medida que o prazo da entrega se aproximou, o volume de demandas concorrentes aumentou bastante. Na Sprint 5, por exemplo, sentimos o impacto do acúmulo de provas e atividades de outras disciplinas, o que resultou em pendências (rollover) de tarefas importantes que estavam planejadas, como a documentação de arquitetura e a conclusão de algumas features.

A equipe precisou se reorganizar rapidamente para não comprometer o escopo da primeira entrega, priorizando o fechamento dos fluxos essenciais (login, integração do client do SIGAA, busca de turmas e carteirinha do RU). Esse momento evidenciou a importância de mantermos uma comunicação constante para identificar gargalos com antecedência. Para as próximas sprints pós-release, precisamos calibrar melhor a estimativa de esforço das tarefas para evitar sobrecargas individuais nas semanas mais puxadas do semestre.

## Descreva uma situação recente de colaboração ou feedback, positiva ou difícil, que marcou sua semana.

Uma situação marcante ocorreu durante a estruturação da documentação de arquitetura do sistema no modelo C4 com PlantUML. Inicialmente, havia sido pensado um fluxo com GitHub Actions para renderizar e commitar automaticamente os diagramas em SVG a cada alteração. Porém, o workflow apresentou inconsistências no CI e estava travando a velocidade com que precisávamos atualizar e revisar os diagramas para a entrega.

Conversando com o time, decidimos simplificar a abordagem: substituí o workflow por um script local em Python (`generate_diagrams.py`) que processa os arquivos `.puml` e gera os SVGs de forma determinística antes do commit. Essa decisão destravou a documentação de arquitetura (`docs/arquitetura.md`), permitindo que a equipe revisasse visualmente os quatro níveis (Contexto, Contêiner e Componentes do Frontend e Backend) sem depender de pipelines externos. Essa experiência reforçou para mim o princípio de que, sob pressão de prazo, soluções locais simples e transparentes costumam ser muito mais eficientes do que automações complexas que geram atrito.

## Que responsabilidades técnicas você tem assumido, e como você tem lidado com elas?

Nesta fase de preparação para a R1, expandi minhas responsabilidades para um escopo fullstack. No backend, implementei a funcionalidade de Configurações Pessoais (`/me`), desenvolvendo desde a persistência nos modelos e repositórios até o serviço de regras de negócio (`settings.py`) e os testes automatizados com `pytest`. No frontend web, assumi a integração desse módulo consumindo os schemas tipados gerados pelo OpenAPI via TanStack Query, além de criar testes automatizados com Vitest.

Também assumi a configuração do manifesto da aplicação (`manifest.json`) para suporte a PWA e, na reta final da release, a criação de uma tela de erro minimalista e resiliente (`ErrorPage.tsx`) com cobertura completa de testes. Lidar com pontas diferentes da aplicação (Python/FastAPI no backend e React/TypeScript no frontend) exigiu alternar contextos técnicos constantemente. Minha estratégia para manter a segurança foi apoiar cada entrega em testes automatizados e no linter `ruff`, garantindo que nenhuma alteração quebrasse contratos prévios de API ou regressões visuais.
