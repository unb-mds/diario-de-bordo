---
title: "Organização da Equipe e Estudos Iniciais — 2026-09-23"
authors:
tags: [primeiro-envio, formacao-equipe, organizacao]
date: 2026-09-23
---

## Descreva como está sendo o processo de organização da sua equipe até agora — papéis, expectativas, primeiras decisões.

Na formação do Grupo G10 para construir o **Glossário UnB** (um dicionário colaborativo de siglas, gírias e expressões da universidade inspirado no `glossario-ufcg`), começamos definindo os papéis e combinando nossos primeiros ritos de acompanhamento. Logo nas reuniões iniciais entre 13/09 e 15/09, estruturamos o projeto em sprints, escolhemos o Ítalo como Scrum Master e a Jéssyca como PO (com Pedro, Allan e eu na equipe de desenvolvimento), criamos a planilha colaborativa para levantar os primeiros termos e partimos juntos para organizar o Story Map no Figma visando a apresentação de 16/09.

Olhando para esses primeiros encontros, percebi na prática que alinhar papéis e estrutura logo no começo evita muita perda de tempo depois, mas também notei um ponto sensível: nem todos conseguimos estar presentes em todas as reuniões registradas nas atas (como as de 13/09, 14/09, 20/09 e 23/09, quando eu mesmo faltei em alguns momentos). Quando alguém fica fora de uma conversa de alinhamento, acaba dependendo de resumos curtos para entender o contexto das decisões. Isso me mostrou que, em um time pequeno, presença constante e registro claro nas atas não são burocracia — são o que mantém todo mundo na mesma página. Para as próximas semanas, pretendo acompanhar todas as decisões registradas no repositório e participar com mais regularidade das reuniões de alinhamento.

## Conte como tem sido o ritmo de trabalho da sua equipe nesta fase de preparação para a primeira entrega.

O ritmo inicial tem sido bem intenso e marcado por ajustes de última hora conforme os prazos da disciplina se aproximam. Um exemplo concreto aconteceu em 14/09 e 15/09: após definirmos as sprints e a planilha inicial, precisamos marcar uma reunião de emergência no dia 15/09 para fechar a organização do Story Map no Figma a tempo da apresentação do dia seguinte, 16/09, e ainda ficaram pendências para terminar depois. Em seguida, com a primeira grande entrega marcada para 28/09 (Release 1), o time precisou correr em paralelo para fechar requisitos, protótipo no Figma e a primeira versão do MVP.

Essa dinâmica deixou evidente que deixar definições acumularem para resolver em reuniões de emergência aumenta a pressão sobre todo o grupo e torna o ritmo irregular. O que tirei dessa experiência é que fatiar o trabalho em entregas menores — em que cada membro assume um bloco bem definido com antecedência — reduz o estresse perto das datas de aula. Quero manter o hábito de quebrar minhas próprias tarefas cedo dentro da sprint para não concentrar tudo na véspera das entregas.

## Que responsabilidades técnicas você tem assumido, e como você tem lidado com elas?

Nesta fase inicial, assumi a tarefa de estudo individual de tecnologia ("coelho da sprint") comparando **React e Vue** para fundamentar a escolha de frontend do projeto, trabalho que registrei no repositório em 15/09 (`docs/estudos/Frontend-react-vue.pdf`). Estudei os modelos de componentes, ecossistema, curva de aprendizado e custo de setup dessas duas alternativas modernas para apresentar ao time o que cada uma traria de benefício ou complexidade.

O mais interessante veio quando cruzamos esse estudo com a realidade do nosso domínio: como o Glossário UnB tem escopo enxuto e foco em simplicidade e offline (PWA), a equipe avaliou que adotar um framework pesado exigiria etapa de build e dependências desnecessárias, optando por **JavaScript e CSS puros** (registrado depois na ADR 0002). Esse episódio mudou minha visão sobre pesquisa técnica: estudar uma tecnologia não serve apenas para defendê-la e usá-la a qualquer custo, mas principalmente para dar base sólida à equipe na hora de decidir se ela realmente se encaixa no problema — inclusive quando a melhor escolha é *não* usá-la. Daqui em diante, vou continuar avaliando o custo-benefício das ferramentas antes de propor código, focando agora em ajudar o grupo com os fluxos de Git e contribuição externa que vêm na sequência.
