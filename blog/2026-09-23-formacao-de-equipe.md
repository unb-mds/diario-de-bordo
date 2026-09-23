---
title: "Formação de equipe - 23/09/2026"
authors: "Kauã Mendes"
tags: [formacao-equipe]
date: 2026-09-23
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

## Descreva como está sendo o processo de organização da sua equipe até agora — papéis, expectativas, primeiras decisões.

_(Nossa organização tomou forma graças ao alinhamento da primeira reunião e aos resultados das sprints 1 e 2. No começo, cada um tinha uma função bem específica, mas logo percebemos que o dia a dia precisava ser mais dinâmico. Isso gerou um ótimo aprendizado, quando um setor está sobrecarregado e outro não, o melhor caminho é agir em equipe para equilibrar as tarefas. Sobre minhas expectativas iniciais, eu achei que focaríamos mais rápido na produção de código (commits), mas logo eu percebi que planejar a base de como o projeto vai funcionar é muito mais importante.)_

## Que sensações ou pensamentos você tem tido em relação ao início desta disciplina e ao projeto que vocês vão desenvolver?

_(Logo no início, achei a matéria um pouco teórica demais e tive certa dificuldade com os primeiros conceitos, especialmente na parte de requisitos. Porém, com o andamento das aulas, consegui pegar o jeito e acompanhar o resto do conteúdo. Sobre o projeto, estou bem otimista. O trabalho está fluindo super bem na medida do possível e a nossa ideia base já está muito bem amadurecida.)_

## Que conhecimentos, ferramentas ou práticas você sente que já domina, e quais ainda são novidade para você neste momento?

_(Acho que já me viro bem com o uso adequado de agentes e com o versionamento do projeto. Em contrapartida, a nossa dinâmica de trabalho diária e a parte de mexer na prática com APIs e banco de dados ainda são novidades que estou explorando e aprendendo, sigo me esforçando ao máximo para abstrair tudo da melhor forma.)_

## Conte como tem sido o ritmo de trabalho da sua equipe nesta fase de preparação para a primeira entrega.

_(As coisas deram uma boa acelerada agora, já que investimos a primeira sprint inteira e um pedaço da segunda focando mais na nossa organização. Mas, mesmo com esse ritmo mais puxado, está aceitável pra acompanhar e dar conta do trabalho.)_

## Descreva uma situação recente de colaboração ou feedback, positiva ou difícil, que marcou sua semana.

_(Nesta semana, foquei na parte visual da documentação da API fazendo dupla com meu colega, e a nossa parceria tem rendido bons resultados. O trabalho ainda não está pronto, mas como a orientação inicial era tirar os primeiros dias para entender a ferramenta e planejar como faríamos, acho que nós dois aproveitamos bem essa fase de estudos. Com essa base, colocar a mão na massa no desenvolvimento direto está sendo bem mais tranquilo e produtivo agora.)_

## Que responsabilidades técnicas você tem assumido, e como você tem lidado com elas?

_(Nessa fase inicial, assumi a responsabilidade técnica de estruturar e implementar a suíte inicial de testes automatizados da nossa API com pytest, em conjunto com a pesquisa de boas práticas de testes que realizei com o Samuel, além de garantir a padronização do código com o linter ruff. Minha tarefa mais marcante foi na branch feat/11-primeiros-testes, onde fiquei responsável por cobrir o fluxo de autenticação e a integração com o módulo externo sigaa-client.Essa experiência me mostrou que assumir a parte de testes exige entender a fundo as decisões de arquitetura dos outros colegas: para testar a rota, precisei entender como o módulo de autenticação estava consumindo o sigaa-client, o que inclusive me levou a identificar e corrigir detalhes nas chamadas desse cliente e a rodar o ruff para manter o código limpo e consistente com o restante do repositório.Para as próximas sprints, pretendo manter a prática de estruturar fixtures reutilizáveis no conftest.py e criar testes com mocks logo após ou durante a criação dos endpoints. Como ponto a melhorar, quero alinhar ainda mais cedo os contratos de interface e os tipos de retorno com os colegas responsáveis pelas features, evitando ter que ajustar chamadas de módulos externos na etapa em que os testes já estão sendo escritos.)_
