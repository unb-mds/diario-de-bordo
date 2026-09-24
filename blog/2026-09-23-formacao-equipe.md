---
title: "Formação de equipe — 2026-09-23"
authors: Arthur Miranda Silva
tags: [formacao-equipe]
date: 2026-09-23
---

## Descreva como está sendo o processo de organização da sua equipe até agora — papéis, expectativas, primeiras decisões.

Minha equipe se formou logo na primeira semana e um dos integrantes sugeriu que fizéssemos o projeto do Cerradinho, e todo mundo concordou. Para separar o que cada um iria fazer, dividimos o trabalho em seis áreas e criamos uma enquete no WhatsApp e cada um tinha que votar em duas áreas de preferência, depois de separarmos o trabalho de cada um, eu fiquei responsável pelo agendamento automático do scraping, log de execuções, rate limiting e cache.

Ao decorrer do projeto, percebi que minha parte depende das pessoas que fazem os scrapers (Vitor e Ítalo) no início é complicado se adequar ao formato que cada um desenvolve sua parte, mas conseguimos nos adequar até que bem após as primeiras reuniões, a mesma coisa ocorreu entre mim e o Gabriel, porque ambos mexemos no docker compose, mas bastou uma ligação para colocarmos tudo em seu devido lugar.

Isso me mostrou que separar cada requisito é tranquilo, mas esconde as dependências entre a parte de cada integrante. Agora, já deixamos separado o que cada um tem que fazer em cada release e estamos derivando isso nas sprints para facilitar o trabalho a longo prazo.

## Que sensações ou pensamentos você tem tido em relação ao início desta disciplina e ao projeto que vocês vão desenvolver?

Eu tava meio receoso, pois é o primeiro projeto que faço com mais de uma pessoa e tem que realmente fazer um planejamento, estruturar cada passo e fazer uma análise de requisitos. Mas até o momento, mesmo passando por umas turbulências, está legal ao desenvolvimento do projeto, principalmente que é um projeto que pode ajudar bastante a comunidade acadêmica, esse foi o principal motivo da escolha do Cerradinho.

Diversas vezes quando estou com um horário vago, não sei qual sala está disponível, e com o desenvolvimento desse projeto pode me ajudar e ajudar diversos estudantes. E mesmo que a dificuldade possa me parar em alguns momentos, eu tenho uma equipe para me ajudar.

## Que conhecimentos, ferramentas ou práticas você sente que já domina, e quais ainda são novidade para você neste momento?

Tenho uma base em Python, mas é a primeira vez que tenho contato com Docker, Celery e Redis. Travei várias vezes tentando entender como cada ferramenta funciona e como elas se conectam, mas estou conseguindo avançar relativamente bem.

Um exemplo foi descobrir que o Redis tem bancos separados, escolhidos só pelo número no final da URL de conexão. Com isso, coloquei o broker do Celery no banco 0 e o result backend no banco 1, para que as filas de tarefas e os resultados não se misturassem. Esse tipo de detalhe só ficou claro quando fui configurar na prática, e não lendo a documentação. Por isso, quero continuar aprendendo cada uma dessas ferramentas para um bom desenvolvimento do projeto.

