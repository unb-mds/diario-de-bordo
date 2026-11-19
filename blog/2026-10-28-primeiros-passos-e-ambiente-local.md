---
title: "Primeiros Passos e Ambiente Local — 2026-10-28"
authors:
tags: [primeiro-envio, ambiente, docsify]
date: 2026-10-28
---

## Que sensações ou pensamentos você tem tido em relação ao início desta disciplina e ao projeto que vocês vão desenvolver?

O início de MDS sempre traz uma expectativa grande e um certo receio em relação ao volume de novas ferramentas, padrões de projeto e rotinas de desenvolvimento que teremos de adotar. No começo, fiquei apreensivo sobre como seria gerenciar tantas exigências técnicas ao mesmo tempo — desde a configuração de ambientes e esteiras até o próprio diário de bordo reflexivo. No entanto, ao dar o primeiro passo prático e começar a configurar este repositório, percebi que boa parte do receio vinha do desconhecimento inicial sobre a estrutura do Docsify e sobre como os arquivos se conectavam. Superar essa primeira barreira me deu mais confiança para encarar o desenvolvimento das próximas fases do projeto.

## Que conhecimentos, ferramentas ou práticas você sente que já domina, e quais ainda são novidade para você neste momento?

Já tenho familiaridade com comandos básicos de terminal, navegação em diretórios e controle de versão com Git. Por outro lado, trabalhar com documentação estática baseada em Markdown renderizada em tempo real (como o Docsify) e lidar com particularidades de políticas de execução do PowerShell no Windows eram pontos com os quais eu não lidava com tanta frequência. Utilizar assistência de IA em pair programming para diagnosticar o ambiente e construir soluções sob medida também é uma prática recente para mim, que se mostrou muito produtiva quando combinada com a leitura crítica das mensagens de erro.

## Descreva uma situação recente de colaboração ou feedback, positiva ou difícil, que marcou sua semana.

Para colocar o diário para rodar localmente no meu computador, decidi trabalhar em conjunto com o assistente de IA no terminal. Ao tentar executar os comandos padrões sugeridos pela documentação oficial (`npx docsify-cli serve .`), nos deparamos com barreiras reais: a política de execução de scripts do PowerShell bloqueou o script `npx.ps1` e o Python não estava configurado no PATH do sistema. 

Em vez de insistir em downloads pesados ou tentar contornar configurações globais arriscadas, analisamos juntos a saída do terminal e vimos que o Node.js puro (v24.16) estava funcionando perfeitamente. A decisão técnica tomada foi criar um servidor HTTP nativo e enxuto (`server.js`) com apenas os módulos internos do Node (`http`, `fs`, `path`), capaz de servir os arquivos do Docsify e os tipos MIME corretos diretamente na porta 3000. 

Essa experiência me mostrou que, no desenvolvimento de software, saber diagnosticar a causa-raiz de um problema de ambiente e encontrar uma alternativa limpa e sem dependências externas é muito mais eficiente do que tentar forçar um comando que não encaixa no cenário da máquina. Para as próximas etapas, vou manter essa postura investigativa: entender o que a ferramenta realmente precisa por baixo dos panos antes de tentar instalar dependências desnecessárias.

## Que responsabilidades técnicas você tem assumido, e como você tem lidado com elas?

Assumi a responsabilidade de garantir que o ambiente local do diário ficasse totalmente operacional e reprodutível. Garanti que qualquer pessoa que clone o projeto possa subir a documentação com um simples comando nativo (`node diario-de-bordo/server.js`), sem exigir dependências globais ou pacotes extras. Também assumi o compromisso de manter o histórico e a navegação do Docsify atualizados, registrando as novas páginas no `_sidebar.md` conforme as instruções da disciplina. Pretendo manter essa disciplina de organização para as entregas de código do nosso projeto principal.

