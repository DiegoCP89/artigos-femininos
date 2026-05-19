# 🔄 BPMN - Processo de Gestão de Inventário

> Este artefato mapeia o fluxo de processos de negócio da loja, destacando a interação entre a proprietária e o novo sistema de inventário.

---

### 🗺️ 1. Diagrama de Processo (Visão Geral)

O fluxo abaixo descreve o processo de **Reposição de Estoque**, desde a chegada da mercadoria até o armazenamento final com auxílio do sistema.

[Diagrama BPMN](https://github.com/DiegoCP89/artigos-femininos/blob/main/documentacao/bpmn.svg)

### 📋 2. Descrição das Etapas

| Atividade | Responsável | Descrição Técnica |
| :--- | :--- | :--- |
| **Receber Mercadoria** | Proprietária | Conferência física das peças enviadas pelo fornecedor. |
| **Cadastrar/Atualizar SKU** | Sistema (C#) | O sistema gera o código único ou soma a quantidade ao saldo existente. |
| **Validar Integridade** | Banco (SQL) | O banco de dados garante que não existam SKUs duplicados. |
| **Gerar Etiqueta** | Sistema (C#) | Impressão ou visualização do código para identificação física. |
| **Armazenar Peça** | Proprietária | Alocação física do acessório no estoque organizado. |

### 🚀 3. Melhorias Identificadas (To-Be)
Com a implementação do BPMN "To-Be" (Como será), eliminamos as seguintes falhas:
* **Fim do registro manual:** Redução de erros de escrita.
* **Gatilho de Alerta:** O sistema avisa automaticamente quando o estoque está baixo, eliminando a necessidade de conferência visual diária.

---

### 📊 Status do Artefato
![Fase](https://img.shields.io/badge/Fase-Projeto-blueviolet) 
![Dificuldade](https://img.shields.io/badge/Dificuldade-M%C3%A9dia-yellow)
