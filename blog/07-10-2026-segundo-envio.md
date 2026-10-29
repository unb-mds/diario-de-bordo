---
title: "segundo-envio — 07/10/2026"
authors: [bcaueLPS]
tags: [segundo-envio]
date: 2026-10-03
---

<!--
Modelo de entrada do diário de bordo. Duplique este arquivo uma vez por fase
(5 no semestre todo), renomeando para algo como
blog/2027-03-10-primeiro-envio.md, e preencha:

- title: nome da fase + data
- tags: marcação temporal: ex: primeiro envio, segundo envio..
- date: data da entrada (YYYY-MM-DD)

O bloco entre "---" acima (front matter) não aparece na tela — ele existe só
para scripts/export-entries.mjs conseguir montar o pacote de dados no fim do
semestre. Não apague nem renomeie essas chaves.

Depois de criar o arquivo, adicione um link para ele em _sidebar.md, na
seção "Minhas entradas", para ele aparecer na navegação do site.

As perguntas completas de cada fase estão em
docs/perguntas.md.
-->

## Conte como tem sido o ritmo de trabalho da sua equipe nesta fase de preparação para a primeira entrega.

Essa semana foi de um ritmo mais intenso, devido ao maior nível de complexidade, como a implementação do código e a integração entre as frentes.

## Descreva uma situação recente de colaboração ou feedback, positiva ou difícil, que marcou sua semana.

Ao fazer o PR de uma branch relacionada à autenticação de usuário para a develop: houve conflitos com a estrutura do banco de dados. Contudo, a situação foi resolvida rapidamente, devido à comunicação back/banco, além disso foi necessário resolver alguns problemas de tratamento de erros. Em grupo foi discutido também o foco do que seria apresentado durante a release 1 o que ajudou bastante na organização.

## Que responsabilidades técnicas você tem assumido, e como você tem lidado com elas?

Fiquei mais focado no epico 01(autenticação e segurança), além da feature 5.1(comentários em cadeiras e turmas). No processo de login/cadastro, correspondente ao épico 01, tive um certo nível de dificuldade, principalmente como toda relação de segurança com o BCRYPT e a integração com o banco. Contudo, vendo exemplos e buscando informações, foi possível implementar. Quanto a feature 5.1, foi mais tranquilo, pois já tinha conseguido pegar uma certa base com o épico 01.
