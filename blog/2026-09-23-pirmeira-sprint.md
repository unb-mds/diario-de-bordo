---
title: Primeira Sprint - 23/09/2026
tags: primeiro envio
date: 2026-09-23
---

# Diário de Bordo - Primeiro Envio
**Nome:** Luiz Guilherme de Alencar Magalhães  
**Projeto:** AvaliaAi (G2-2026-2)  

## Atividades Realizadas

Durante estas primeiras semanas de projeto, o nosso foco dividiu-se entre a idealização visual da aplicação e a construção da arquitetura base do backend. As minhas principais contribuições foram:

### 1. Design e Planeamento (Figma)
* **Prototipagem:** Concluímos o design e as telas do painel no Figma, estruturando a interface visual e a experiência do utilizador.
* **Documentação Base:** Auxiliei na definição da Visão Geral do projeto, na escolha da *stack* tecnológica (Python, Flask, SQLite), na distribuição dos papéis da equipa e no mapeamento do cronograma.

### 2. Desenvolvimento do Backend (Sprint Atual)
Hoje, dediquei-me à reconstrução do repositório e à implementação de toda a camada de dados e de domínio:
* **Issue #24 (Modelo e Base de Dados):** Criei a entidade `Usuario` (`models.py`) e o script de inicialização do SQLite (`database.py`), configurando as tabelas e garantindo o relacionamento relacional (chave estrangeira) com as avaliações.
* **Issue #33 (Modelo de Avaliações):** Estruturei a classe `Avaliacao`, incluindo o método de serialização `to_dict()`.
* **Issue #25 (Persistência):** Implementei o `UsuarioRepository` (`repositorio.py`) para tratar as inserções no SQLite, buscar utilizadores por ID e capturar exceções como `sqlite3.IntegrityError` para evitar e-mails duplicados.
* **Issue #43 (Testes Automatizados):** Criei testes unitários (`test_avaliacoes.py`) com o módulo `unittest`, utilizando uma base de dados em memória (`:memory:`) para validar a inserção e leitura das avaliações de forma isolada.

## Dificuldades Encontradas e Aprendizagens

* **Fluxo de Trabalho com Git:** Tive de lidar com um conflito de *merge* no ficheiro `models.py` durante a Issue #33, pois a minha *branch* local não estava sincronizada com a remota. Resolvi o problema diretamente pelo editor de conflitos do GitHub, o que consolidou bastante o meu entendimento sobre versionamento.
* **Arquitetura de Software:** Criar o projeto desde o primeiro ficheiro obrigou-me a ter cuidado com a separação de responsabilidades (Modelos vs. Repositórios vs. Base de Dados), mas clarificou muito a forma como os componentes de uma API comunicam entre si.