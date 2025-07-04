﻿# Projeto: Gerenciador de Tarefas v2.0

## 1. Visão Geral

Este é um projeto de um Gerenciador de Tarefas via terminal, desenvolvido em Python. A base do projeto oferece funcionalidades para adicionar, listar, concluir e remover tarefas. O objetivo deste trabalho é estender a funcionalidade do sistema e demonstrar um fluxo de trabalho de desenvolvimento profissional utilizando Git e GitHub.

## 2. Configuração Inicial

1.  **Fork:** Realize um fork deste repositório para a sua conta pessoal no GitHub.
2.  **Clone:** Clone o repositório que você criou (o seu fork) para o seu ambiente de desenvolvimento local.
    ```bash
    git clone [https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git](https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git)
    ```

## 3. Especificações da Tarefa

Você deve implementar as **duas** novas funcionalidades descritas abaixo.

### Funcionalidade 1: Prioridade de Tarefas

* **Estrutura de Dados:** A estrutura de dados de cada tarefa deve ser alterada para incluir um campo `prioridade`.
* **Adicionar Tarefa:** A função de adição deve ser modificada para solicitar ao usuário um nível de prioridade (`Alta`, `Média`, `Baixa`). Uma entrada inválida deve resultar na prioridade padrão `Baixa`.
* **Listar Tarefas:** A função de listagem deve ser atualizada para exibir a prioridade de cada tarefa.

### Funcionalidade 2: Edição de Descrição da Tarefa

* **Menu:** Uma nova opção para "Editar Tarefa" deve ser adicionada ao menu principal.
* **Implementação:** Deve ser criada uma função que permita ao usuário:
    1.  Selecionar uma tarefa existente pelo seu índice.
    2.  Visualizar a descrição atual.
    3.  Inserir uma nova descrição para substituí-la.
* **Feedback:** O sistema deve informar ao usuário se a operação foi bem-sucedida.

## 4. Requisitos de Entrega e Fluxo de Trabalho

A avaliação levará em conta a organização do seu repositório e o uso correto das ferramentas.

* **README.md:** Este arquivo deve ser atualizado com a seção "Minhas Contribuições" devidamente preenchida.
* **`.gitignore`:** O repositório precisa conter um arquivo `.gitignore` configurado adequadamente para projetos Python, ignorando arquivos e pastas como `__pycache__` e `venv/`.
* **Fluxo com Branches:** Cada uma das duas funcionalidades deve ser desenvolvida em uma *feature branch* separada (ex: `feature/task-priority` e `feature/edit-task-description`). Após a finalização, cada branch deve ser mesclada (`merge`) de volta à branch `main`.
* **Histórico de Commits:** É exigido um histórico com um mínimo de **8 a 10 commits atômicos**. As mensagens de commit devem ser claras e refletir o trabalho realizado em cada etapa.

## 5. Critérios de Avaliação

* **README:** Clareza e detalhamento da seção "Minhas Contribuições".
* **Git:** Qualidade das mensagens de commit e demonstração do fluxo de trabalho com branches e merges.
* **Funcionalidade:** Implementação correta e funcional das modificações solicitadas.
* **Código:** Legibilidade, organização e qualidade geral do código implementado.

---

## Minhas Contribuições

* **Nome:** João Pedro Chimello Goulart
* **GitHub:** https://github.com/Joaoo0Pedro

### Modificação 1: Prioridade de Tarefas

**Lógica Implementada:**
* Adicionado o campo "prioridade" ao criar tarefas (Alta, Média, Baixa).
* É pedido a prioridade sobre a tarefa, quando adicionada.
* Caso usuario não coloque prioridade ou a que for colocar seja invalida, a tarefa terá o valor "Baixa".
* A função listar_tarefas foi modificada para exibir a prioridade junto à descrição.
* Criada a nova função editar_tarefa, permitindo alterar descrição e prioridade.
* Adicionada a opção "5. Editar Tarefa" no menu principal.

**Como Testar:**
1. Adicionar uma nova tarefa com prioridade.
* Escolha a opção 1. para adicionar uma tarefa.
* Digite uma descrição (ex: Estudar Python).
* Digite a prioridade (ex: Alta, Média ou Baixa).
* Após isso verifique a mensagem de confirmação: Tarefa 'Estudar Python' adicionada com sucesso!

2. Adicionar uma tarefa com prioridade inválida
* Escolha a opção 1 novamente.
* Insira uma descrição.
* Digite algo inválido na prioridade (ex: urgente, 123, ou apenas deixe vazio).
* O programa deve exibir: Prioridade inválida. Definida como 'Baixa' por padrão.

3. Listar tarefas
* Escolha a opção 2. Listar Tarefas.
* Verifique se a lista mostra:
    * Status da tarefa de concluido ou em branco
    * Descrição
    * Prioridade definida (Alta, Média, Baixa)

### Modificação 2: Editar Descrição da Tarefa

**Lógica Implementada:**
* Criada a função editar_tarefa() para alterar descrição e prioridade de uma tarefa.
* Adicionada a opção "5. Editar Tarefa" no menu principal.
* O usuário informa o número da tarefa, uma nova descrição e uma nova prioridade.
* A prioridade é validada; se inválida, assume "Baixa" com aviso.
* Os campos "descricao" e "prioridade" são atualizados diretamente na lista.
* Exibida mensagem de sucesso após a edição.
* O código principal (main()) foi ajustado para chamar a função de edição.

**Como Testar:**
1. Editar uma tarefa existente
* Escolha a opção 5. Editar Tarefa.
* Digite o número da tarefa que deseja editar.
* Altere a descrição e a prioridade.
* Verifique se:
    * A tarefa foi atualizada corretamente.
    * A prioridade é validada novamente (como na adição).
