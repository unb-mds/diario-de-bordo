---
title: "Criação da api de web scraping do sigaa - 28/10/2026"
authors: [Vitor Piau Morhy]
tags: [scraping, api, python, fastapi]
date: 2026-10-28
---

**Que responsabilidades técnicas você tem assumido, e como você tem lidado com elas?**

Neste último mês, assumi a responsabilidade de extrair os dados reais das disciplinas diretamente do SIGAA. Como o sistema não fornece uma API pública e documentada, a única solução foi construir um sistema de *web scraping* do zero. Para isso, decidi utilizar Python em conjunto com o framework FastAPI. Antes de começar a programar a API definitiva, percebi que precisava estudar a fundo o funcionamento das requisições HTTP e a estrutura do DOM (Document Object Model) das páginas do sistema da faculdade. LIdei com isso aprendedno o funcionamnto de um web scrapig e de uma api, e entao coloquei a mão na massa, errei varias vezes e tive varias dificuldadaes para fazer a api funcionar, tambem utilizei o gemini pra me ajudar a corrigir e estruturar da forma correta.

**Descreva como as decisões técnicas estão sendo tomadas na sua equipe nesta fase — quem decide, como se chega a um consenso.**

Nesta fase do projeto, as decisões foram tomada pela viabilidade e qualidade do resultado. Um ótimo exemplo foi justamente a escolha de como obteríamos os dados das disciplinas. Ao perceber a ausência de uma API oficial do SIGAA, pesquisamos alternativas e descobrimos o *web scraping*. Na nossa equipe, as decisões são baseadas na concordância de todos pelo que será a melhor opção. O consenso foi alcançado rapidamente quando a equipe viu, ao usarmos o FastAPI para fazermos a api de *web scraping*, nós teriamos acesso a uma documentação nativa e interativa via Swagger que facilitaria o processo. Na nossa dinâmica atual, qualquer um pode levantar as possibilidades tecnológicas, mas a decisão final é tomada em conjunto.

**Que lacunas técnicas ainda te incomodam, e o que você tem feito, ou pretende fazer, a respeito?**

O que mais me incomodou, e revelou uma lacuna técnica na minha formação, foi a dificuldade em lidar com a imprevisibilidade do *web scraping*. O HTML do SIGAA é bastante antigo, estruturado em tabelas complexas e muitas vezes sem identificadores claros (IDs ou classes). Percebi que eu não sabia ao certo como garantir a constancia do código: se a estrutura mudasse ligeiramente ou se a página demorasse a carregar, a nossa API podia falhar e derrubar o back-end inteiro. Para resolver isso, resolvi usar um banco de dados, assim o scraping so precisa ser feito quando for necessario atualizar os dados, os quais ficam armazenados em um banco de dados e a api busca direto do banco de dados. Outro problema sera a integração com o front da maneira correta, e a identificação de materias equivalentes, pontos nos quais ainda estudou estudando no momento, visando resolver em um futuro próximo