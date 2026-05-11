# 📱 Documentação de Portabilidade

> Este documento descreve os requisitos e as diretrizes para garantir que o sistema de inventário digital possa ser executado e implantado em diferentes ambientes tecnológicos.

---

### 🛠️ 1. Ambiente de Execução (Runtime)
O sistema é desenvolvido utilizando o framework `.NET`, o que permite alta portabilidade através do conceito de *multi-plataforma*:
* **Sistemas Operacionais Suportados:** Windows 10/11, distribuições Linux (via Docker/Runtime .NET) e macOS.
* **Dependências de Software:** Requer a instalação do `.NET Runtime 6.0` ou superior no ambiente de destino.

### 🗄️ 2. Portabilidade de Dados
A arquitetura do sistema utiliza o **Entity Framework Core (ORM)** para a comunicação com o banco de dados, o que garante:
* **Independência de SGBD:** O sistema está configurado inicialmente para `PostgreSQL`, mas pode ser portado para `SQL Server` ou `SQLite` apenas alterando a *Connection String* e o provedor no arquivo de configuração, sem modificar a lógica de negócio.
* **Migrações:** O uso de *Migrations* permite que a estrutura do banco de dados seja recriada em qualquer servidor compatível de forma automática.

### 🌐 3. Portabilidade de Interface (Acesso)
Para garantir que a proprietária acesse o sistema de diferentes dispositivos:
* **Navegadores:** Compatibilidade total com Google Chrome, Mozilla Firefox e Microsoft Edge (padrão ECMAScript 6+).
* **Responsividade:** A interface deve adaptar-se a resoluções de monitores padrão (1366x768) e tablets, garantindo a legibilidade do inventário em dispositivos móveis.

### 📦 4. Estratégia de Implantação
Para facilitar a portabilidade entre servidores de desenvolvimento e produção:
* **Containerização:** O projeto prevê suporte a `Docker`, permitindo que toda a aplicação e suas dependências sejam empacotadas em um container isolado, garantindo que "rode em qualquer lugar".

---

### 📊 Status do Artefato
![Fase](https://img.shields.io/badge/Fase-Elicita%C3%A7%C3%A3o-orange) 
![Dificuldade](https://img.shields.io/badge/Dificuldade-F%C3%A1cil-green)

---
