# 🔗 Matriz de Rastreabilidade de Requisitos

> Este documento vincula as necessidades elicitadas às regras de negócio e prepara a transição para os diagramas de caso de uso.

---

### 1. Requisitos x Regras de Negócio (RN)

| ID Requisito | Descrição do Requisito | Regra de Negócio Vinculada |
| :--- | :--- | :--- |
| **RF01** | O sistema deve gerar SKUs automáticos. | **RN01:** O SKU deve seguir o padrão `CATEGORIA-ID-ANO`. |
| **RF02** | O sistema deve emitir alertas de estoque. | **RN02:** Alerta disparado quando saldo for $\leq 3$. |
| **RF03** | Cadastro de Preço de Custo e Venda. | **RN03:** O valor de venda não pode ser menor que o de custo. |

### 2. Requisitos x Casos de Uso (UC)

| ID Requisito | Caso de Uso (Futuro) | Objetivo da Funcionalidade |
| :--- | :--- | :--- |
| **RF01 / RF03** | `UC01 - Manter Produto` | Permitir inclusão e edição de peças no inventário. |
| **RF02** | `UC02 - Consultar Alertas` | Visualizar itens que necessitam de reposição. |
| **RF04** | `UC03 - Registrar Movimentação` | Somar ou subtrair itens do saldo real. |

---

### 📊 Status do Artefato
![Fase](https://img.shields.io/badge/Fase-Elicita%C3%A7%C3%A3o-orange) 
![Dificuldade](https://img.shields.io/badge/Dificuldade-M%C3%A9dia-yellow)
