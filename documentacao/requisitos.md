# 📋 Documentação de Requisitos de Software

> Este documento especifica formalmente os requisitos funcionais e não funcionais do Sistema de Gestão de Inventário, servindo como guia para as fases de codificação e testes.

---

### ⚙️ 1. Requisitos Funcionais (RF)

Os requisitos funcionais descrevem as ações, comportamentos e informações que o sistema deve processar.

| ID | Nome do Requisito | Descrição | Prioridade |
| :--- | :--- | :--- | :--- |
| **RF01** | Gerenciamento de Produtos | O sistema deve permitir o cadastro, alteração, consulta e exclusão (CRUD) de acessórios, contendo: Nome, Preço de Custo, Preço de Venda, Categoria, Fornecedor e Foto. | **Essencial** |
| **RF02** | Geração Automática de SKU | O sistema deve gerar o código SKU de forma automática no momento do cadastro, seguindo o padrão estabelecido na RN01 (`[CATEGORIA]-[ID]-[ANO]`). | **Essencial** |
| **RF03** | Registro de Movimentação | O sistema deve registrar entradas (compras/reposições) e saídas (vendas/baixas) de itens, atualizando o saldo em tempo real. | **Essencial** |
| **RF04** | Alerta de Estoque Mínimo | O sistema deve emitir um alerta visual na tela principal sempre que o saldo de um produto for igual ou inferior a 3 unidades. | **Importante** |
| **RF05** | Controle de Acesso (Login) | O sistema deve autenticar os usuários via CPF e senha, restringindo telas administrativas apenas para o perfil de Proprietária. | **Essencial** |
| **RF06** | Relatório de Giro de Estoque | O sistema deve gerar relatórios financeiros e gráficos demonstrando o valor total investido em estoque e o lucro estimado baseado nas vendas. | **Importante** |

---

### 🛠️ 2. Requisitos Não Funcionais (RNF)

Os requisitos não funcionais definem os critérios de qualidade, restrições tecnológicas e usabilidade do sistema.

| ID | Categoria | Descrição | Prioridade |
| :--- | :--- | :--- | :--- |
| **RNF01** | Tecnologia / Linguagem | O sistema deve ser desenvolvido utilizando o framework **.NET Core 6.0 (ou superior)** com a linguagem C#. | **Essencial** |
| **RNF02** | Banco de Dados | A persistência dos dados deve ser feita no SGBD relacional **PostgreSQL**, utilizando o Entity Framework Core como ORM. | **Essencial** |
| **RNF03** | Segurança | Todas as senhas de usuários cadastradas devem ser criptografadas (hashing) antes de serem salvas no banco de dados. | **Essencial** |
| **RNF04** | Usabilidade | A interface do usuário deve ser limpa e responsiva, permitindo a operação fluida em monitores desktop padrão e tablets. | **Importante** |
| **RNF05** | Desempenho | As consultas ao banco de dados para listagem do inventário não devem exceder o tempo de resposta de 2 segundos sob condições normais de rede. | **Importante** |

---

### 📊 Status do Artefato
![Fase](https://img.shields.io/badge/Fase-Projeto-blueviolet) 
![Dificuldade](https://img.shields.io/badge/Dificuldade-M%C3%A9dia-yellow)

---
