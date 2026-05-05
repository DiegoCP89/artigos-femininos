# ❓ Perguntas e Respostas para Elicitação de Requisitos

> Este documento registra a entrevista realizada com a stakeholder principal para levantamento das necessidades funcionais e não funcionais do sistema de inventário.

---

### 👤 Identificação
* **Entrevistador:** Diego Cruz Pereira / João Pedro Ishida
* **Entrevistado:** Proprietário da Loja de Acessórios
* **Data:** __ /__ /____
* **Técnica Utilizada:** Entrevista Semiestruturada

---

### 💬 Roteiro de Perguntas e Respostas

#### 1. Sobre o Cadastro de Produtos
* **Pergunta:** Quais informações são indispensáveis ao cadastrar uma nova peça?
* **Resposta:** Preciso do nome da peça, categoria (brinco, anel, colar), material (prata, folheado), preço de custo, preço de venda e o nome do fornecedor.

#### 2. Sobre o Controle de Estoque (SKU)
* **Pergunta:** Como você gostaria que o sistema gerasse os códigos dos produtos?
* **Resposta:** Atualmente não temos padrão. Gostaria que o sistema gerasse um código único (SKU) automaticamente para cada variação de peça.

#### 3. Sobre a Operação de Vendas e Entradas
* **Pergunta:** Como deve ser o registro quando uma peça é vendida ou quando chega reposição?
* **Resposta:** Preciso de uma tela simples onde eu informe o código da peça e a quantidade. O sistema deve subtrair na venda e somar na entrada de estoque automaticamente.

#### 4. Sobre Alertas e Relatórios
* **Pergunta:** Qual o nível crítico de estoque para você ser avisada?
* **Resposta:** Quando uma peça chegar a 3 unidades, o sistema deve me mostrar um alerta visual em vermelho para eu fazer o pedido ao fornecedor.
* **Pergunta:** Qual relatório é mais importante para o seu dia a dia?
* **Resposta:** Um relatório que me mostre quais peças não estão saindo (estoque parado) e o valor total investido em mercadoria.

#### 5. Sobre Segurança e Acesso
* **Pergunta:** Quem terá acesso ao sistema?
* **Resposta:** Apenas eu e meu sócio. Cada um deve ter sua senha para evitar que pessoas não autorizadas vejam os lucros.

---

### 📋 Principais Descobertas (Insights)
* **Prioridade Alta:** Automação do cálculo de saldo e alertas de estoque mínimo.
* **Necessidade Técnica:** O banco de dados deve suportar fotos das peças para facilitar a identificação visual no cadastro.
* **Restrição:** A interface deve ser extremamente simples, focada em rapidez, já que a cliente atende e registra ao mesmo tempo.

---

### 📊 Status do Artefato
![Fase](https://img.shields.io/badge/Fase-Elicita%C3%A7%C3%A3o-orange) 
![Dificuldade](https://img.shields.io/badge/Dificuldade-M%C3%A9dia-yellow)

---
