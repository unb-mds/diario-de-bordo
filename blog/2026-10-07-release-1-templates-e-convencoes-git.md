---
title: "Release 1, Templates e Convenções Git — 2026-10-07"
authors:
tags: [segundo-envio, release-1, git, feedback]
date: 2026-10-07
---

## Olhando para a release que acabou de ser entregue, o que você diria que funcionou bem e o que não funcionou na sua equipe?

Na entrega da **Release 1** (em 28/09), conseguimos colocar de pé um protótipo funcional sólido para o Glossário UnB: fechamos um schema único de dados validado automaticamente no navegador e no CI (ADR 0004), construímos o aplicativo PWA em JavaScript e CSS puros sem build (ADRs 0002 e 0003), com busca em tempo real e filtros por tipo e campus, além de substituir os termos de exemplo por 41 termos reais com fonte verificada. Esse alinhamento entre arquitetura simples e validação automática no repositório foi o que funcionou melhor, porque deu segurança de que qualquer termo novo seguiria o mesmo padrão.

Por outro lado, a organização do fluxo de entregas deixou a desejar na reta final da R1. Grande parte das contribuições — inclusive as minhas, como a formalização da convenção de commits e branches (`#17`), o primeiro rascunho da constituição do projeto e os templates de issue (`#24` / PR `#29`) — acabou subindo concentrada no próprio dia 28/09. Como consequência, alguns Pull Requests ficaram abertos esperando revisão ou merge depois da data, e também escaparam detalhes nos dados iniciais, como as siglas dos campi externos (`FCTS`, `FCTE` e `FUP`) cadastradas com `campus: "Geral"`, o campo `categoria` ainda aberto sem lista fechada na ADR 0004 e as coordenadas do `Ceubinho` sem conferência no mapa. Isso me mostrou que código rodando não basta se o fluxo de revisão e a qualidade dos dados não acompanharem o mesmo ritmo. Para a fase seguinte, o foco passa a ser abrir PRs menores com antecedência e revisar os dados com o mesmo rigor do código.

## Como o feedback recebido (de colegas, professora, monitoria) tem influenciado o que vocês estão fazendo agora?

Os retornos que recebemos após a Release 1 e nas revisões internas apontaram lacunas bem objetivas no projeto: faltava organizar semanticamente os termos em categorias fechadas, corrigir a qualidade e redação dos dados já cadastrados, melhorar o guia de instalação/ambiente no README e estruturar uma coleta mais escalável do que a planilha manual. Em vez de tratar essas críticas de forma solta, a equipe transformou cada ponto em épicos e issues concretas no planejamento das Sprints 04 a 09.

Essa resposta estruturada ao feedback está guiando exatamente no que vou trabalhar na preparação da Release 2: já mapeamos a correção dos termos existentes (`#65`), a definição da taxonomia fechada de categorias (`#63`) e o amadurecimento dos formulários de contribuição externa (`#71`), além das diretrizes de qualidade no CI e do registro transparente do uso de IA no `AI-USAGE.md`. Ver as críticas da R1 virarem critérios de aceitação testáveis me fez perceber que feedback em engenharia de software só gera evolução quando se traduz em tarefas rastreáveis no backlog. A partir de agora, quero olhar para cada apontamento de revisão já pensando em qual regra ou teste automatizado garante que o problema não volte a acontecer.

## Descreva uma situação recente de colaboração ou feedback, positiva ou difícil, que marcou sua semana.

Um episódio muito marcante dessa etapa envolveu a criação dos templates de contribuição externa (`adicionar-termo.md` e `corrigir-definicao.md`) para atender à issue `#24`, que abri no PR `#29`. A ideia dos templates era permitir que qualquer pessoa da UnB que não soubesse usar Git pudesse sugerir ou corrigir um termo abrindo uma issue, e nós testamos ambos na prática com as issues `#30` (sobre o `Ceubinho`) e `#31`.

Quando confrontamos o template com o schema único definido na ADR 0004, porém, apareceu um desalinhamento claro: no campo `Tipo` de `adicionar-termo.md`, incluímos a opção `local`, sendo que a função de validação (`validacao-termo.js`) só aceita `sigla`, `giria` e `expressao` — um lugar físico entra com um desses tipos somado à categoria `locais-campus` e ao objeto opcional `localizacao`. Além disso, deixamos um link de exemplo temporário (`https://exemplo.com/canal-do-grupo`) no `config.yml`. Essa situação mostrou que não basta um formulário parecer intuitivo para quem escreve a issue: se ele induzir o usuário a preencher valores que o código recusa, gera retrabalho para quem vai integrar o termo. Como encaminhamento concreto, isso já nos deu base para planejar a evolução desses arquivos para **Issue Forms em YAML** com campos obrigatórios e menus fechados alinhados diretamente às constantes do schema.
