# 📏 Métricas de Custo (Baseadas em Modelagem de Dados)

> Este documento estabelece a métrica de custo do projeto utilizando como base a complexidade das entidades e relacionamentos que compõem a arquitetura do sistema.

---

### 📊 1. Estimativa por Complexidade de Entidades (DER/Diagrama de Classes)
O investimento total de **R$ 15.000,00** é fundamentado no esforço técnico para modelar, normalizar e implementar as seguintes estruturas no banco de dados `PostgreSQL`:

| Entidade (Classe/Tabela) | Complexidade Técnica | Peso no Custo | Justificativa de Modelagem |
| :--- | :--- | :--- | :--- |
| **Produto / SKU** | Alta | 35% | Requer atributos complexos, chaves estrangeiras múltiplas e normalização (3FN). |
| **Movimentação / Estoque** | Alta | 35% | Entidade associativa de alta transacionalidade com lógica de integridade referencial. |
| **Fornecedor / Cliente** | Média | 15% | Estrutura de cadastros com relacionamentos 1:N padronizados. |
| **Usuário / Perfil** | Baixa | 15% | Entidade de controle de acesso com atributos simples e poucas relações. |

### 💰 2. Distribuição Financeira por Esforço de Dados
Abaixo, a decomposição do valor baseada nas camadas de dados e lógica do sistema em `C#`:

* **Implementação de Arquitetura de Dados (DDL/DML):** R$ 7.500,00
  * *Criação de tabelas, índices e relacionamentos baseados no DER.*
* **Lógica de Persistência e Regras de Negócio:** R$ 4.500,00
  * *Desenvolvimento das classes em C# que garantem a integridade dos dados.*
* **Otimização e Queries de Relatórios:** R$ 3.000,00
  * *Extração de dados complexos para giro de estoque e alertas.*

### ⚡ 3. Métricas de Desempenho
* **Tempo de Resposta:** Consultas ao banco de dados não devem exceder 2 segundos.
* **Disponibilidade:** O sistema deve estar disponível 99% do tempo (considerando ambiente Cloud).

---

### 📊 Status do Artefato
![Fase](https://img.shields.io/badge/Fase-Planejamento-blue) 
![Dificuldade](https://img.shields.io/badge/Dificuldade-Elevada-red)

---
