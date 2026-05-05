# 🔗 Matriz de Rastreabilidade de Requisitos

> Este documento estabelece a conexão entre as necessidades da cliente (elicitadas na entrevista), as regras de negócio do sistema e os futuros casos de uso, garantindo que 100% do escopo seja atendido.

---

### 🎯 1. Rastreabilidade: Requisitos x Regras de Negócio (RN)
Esta tabela garante que cada funcionalidade solicitada respeite as diretrizes operacionais da loja.

| ID | Requisito Funcional (RF) | Regra de Negócio (RN) Relacionada | Descrição da RN |
| :--- | :--- | :--- | :--- |
| **RF01** | Gerar código SKU automático. | **RN01 - Padronização** | O SKU deve ser único e gerado concatenando [CATEGORIA]-[ID]-[ANO]. |
| **RF02** | Registrar entrada/saída de itens. | **RN02 - Cálculo de Saldo** | Toda saída deve validar se o saldo atual é maior ou igual à quantidade vendida. |
| **RF03** | Cadastro de Preços (Custo/Venda). | **RN03 - Margem Mínima** | O sistema deve impedir que o preço de venda seja inferior ao preço de custo. |
| **RF04** | Alerta de estoque mínimo. | **RN04 - Gatilho de Alerta** | O alerta visual deve ser disparado obrigatoriamente quando o saldo for $\leq 3$ unidades. |
| **RF05** | Controle de Acesso Restrito. | **RN05 - Hierarquia** | Somente usuários com perfil 'Administrador' podem visualizar relatórios de lucro. |

---

### 🔄 2. Rastreabilidade: Requisitos x Casos de Uso (UC)
Esta tabela prepara o terreno para a próxima fase de Design, mapeando o que o sistema fará.

| ID Requisito | Caso de Uso (UC) | Nome do Caso de Uso | Objetivo |
| :--- | :--- | :--- | :--- |
| **RF01, RF03** | `UC01` | **Manter Produto** | Permitir o CRUD (Criar, Ler, Atualizar e Deletar) de peças de acessórios. |
| **RF02** | `UC02` | **Registrar Movimentação** | Processar as entradas de fornecedores e baixas de vendas no estoque. |
| **RF04** | `UC03` | **Consultar Alertas** | Exibir para a proprietária a lista de itens que precisam de reposição imediata. |
| **RF05** | `UC04` | **Autenticar Usuário** | Garantir login seguro via CPF/Senha para acesso administrativo. |
| **RF04, RF02** | `UC05` | **Gerar Relatórios** | Extrair dados de giro de estoque e valor total investido. |

---

### 📋 Considerações Técnicas
* **Consistência:** A matriz confirma que o requisito de "Fotos das peças" (elicitado na entrevista) será atendido dentro do `UC01 - Manter Produto`.
* **Risco de Escopo:** Não foram identificados requisitos órfãos (sem funcionalidade) ou funcionalidades sem um requisito que as justifique.

---

### 📊 Status do Artefato
![Fase](https://img.shields.io/badge/Fase-Elicita%C3%A7%C3%A3o-orange) 
![Dificuldade](https://img.shields.io/badge/Dificuldade-M%C3%A9dia-yellow)

---
