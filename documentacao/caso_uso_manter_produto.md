# 📄 Documentação de Caso de Uso: UC01 — Manter Produto

> Este documento detalha as interações, cenários de sucesso, extensões e fluxos de exceção para o gerenciamento (CRUD) de acessórios no sistema de inventário.

---

### 🔍 1. Ficha Técnica do Caso de Uso

| Atributo | Descrição |
| :--- | :--- |
| **Identificador** | `UC01` |
| **Nome** | Manter Produto (Acessório) |
| **Atores** | Proprietário (Ator Principal) |
| **Sumário** | Permite o cadastro, consulta, atualização e exclusão de itens de acessórios femininos no banco de dados. |
| **Pré-condições** | O usuário deve estar autenticado no sistema (`UC04`). |
| **Pós-condições** | O estoque é atualizado no banco PostgreSQL e as alterações ficam visíveis no painel. |

---

### 🔄 2. Fluxo Principal (Cenário de Sucesso - Cadastro)

1. A Proprietário acessa o menu "Produtos" e clica em "Novo Produto".
2. O sistema exibe o formulário de cadastro em branco.
3. A Proprietário preenche os campos obrigatórios (Nome, Preço de Custo, Preço de Venda, Categoria, Fornecedor).
4. O sistema gera automaticamente o **SKU** seguindo a regra `RN01` (`[CATEGORIA]-[ID]-[ANO]`).
5. A Proprietário clica em "Salvar".
6. O sistema valida os dados, persiste as informações no banco PostgreSQL via Entity Framework Core e exibe a mensagem: *"Produto Cadastrado com Sucesso!"*.

---

### 🛠️ 3. Fluxos Alternativos e de Exceção

#### **Fluxo Alternativo A: Upload de Foto (Opcional - `<<extend>>`)**
* **Passo 3.1:** No momento do preenchimento, a Proprietária decide anexar uma imagem do acessório.
* **Passo 3.2:** O sistema valida se o arquivo é uma imagem válida (PNG/JPG) e armazena o caminho do arquivo.
* **Passo 3.3:** O fluxo retorna ao passo 5 do fluxo principal.

#### **Fluxo de Exceção B: Dados Obrigatórios Ausentes**
* **Passo 4.1:** O sistema identifica que um ou mais campos obrigatórios não foram preenchidos.
* **Passo 4.2:** O sistema interrompe a persistência e exibe o alerta: *"Erro: Preencha todos os campos obrigatórios antes de continuar"*.
* **Passo 4.3:** O formulário permanece aberto para correção.

#### **Fluxo de Exceção C: Margem de Lucro Inválida (RN03)**
* **Passo 4.1:** O sistema identifica que o Preço de Venda inserido é menor ou igual ao Preço de Custo.
* **Passo 4.2:** O sistema bloqueia a gravação e exibe o alerta: *"Erro: O preço de venda não pode ser inferior ao preço de custo"*.

---

### 📊 Status do Artefato
![Fase](https://img.shields.io/badge/Fase-Projeto-blueviolet) 
![Dificuldade](https://img.shields.io/badge/Dificuldade-M%C3%A9dia-yellow)

---
