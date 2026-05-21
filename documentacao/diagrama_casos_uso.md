# 🗺️ Diagrama de Casos de Uso (UML)

> Este artefato delimita o escopo do sistema, mapeando quais atores interagem com as funcionalidades oferecidas pela aplicação de inventário.

---

### 🖼️ 1. Mapeamento de Escopo e Atores
O diagrama abaixo representa a fronteira do sistema e as interações da Proprietária com os módulos de gerenciamento, movimentação e alertas.

[Diagrama de Casos de Uso](documentacao/diagrama-caso-uso.svg)

### 📋 2. Relacionamentos de Extensão e Inclusão
* **`<<include>>` (Inclusão Obrigatória):** O caso de uso `Registrar Movimentação` inclui obrigatoriamente a validação de saldo no banco de dados para evitar inconsistências.
* **`<<extend>>` (Extensão Opcional):** O caso de uso `Manter Produto` pode disparar a funcionalidade de "Fazer Upload de Foto do Acessório" apenas se o usuário desejar.

---

### 📊 Status do Artefato
![Fase](https://img.shields.io/badge/Fase-Projeto-blueviolet) 
![Dificuldade](https://img.shields.io/badge/Dificuldade-F%C3%A1cil-green)

---
