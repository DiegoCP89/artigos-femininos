# 📏 Métricas de Software

> Este documento define os indicadores e métricas utilizados para mensurar o tamanho, a qualidade e o desempenho do sistema de inventário.

---

### 🔍 1. Métrica de Tamanho (Funcionalidades)
Utilizaremos uma adaptação de contagem por funcionalidades principais para estimar o esforço de desenvolvimento em `C#`:

| Módulo | Complexidade | Estimativa de Esforço |
| :--- | :--- | :--- |
| Cadastro de Produtos (SKU) | Média | 12 horas |
| Controle de Entradas/Saídas | Alta | 20 horas |
| Geração de Relatórios | Média | 10 horas |
| Alertas de Estoque Mínimo | Baixa | 06 horas |

### 🎯 2. Métricas de Qualidade
Para garantir que o sistema atenda às expectativas da loja de acessórios:
* **Taxa de Erro no Inventário:** O objetivo é reduzir a divergência entre o físico e o digital para < 1%.
* **Cobertura de Código:** Mínimo de 70% de cobertura de testes unitários nas regras de negócio.
* **Usabilidade:** O tempo médio para cadastrar um novo produto não deve ultrapassar 60 segundos.

### ⚡ 3. Métricas de Desempenho
* **Tempo de Resposta:** Consultas ao banco de dados não devem exceder 2 segundos.
* **Disponibilidade:** O sistema deve estar disponível 99% do tempo (considerando ambiente Cloud).

---

### 📊 Status do Artefato
![Fase](https://img.shields.io/badge/Fase-Planejamento-blue) 
![Dificuldade](https://img.shields.io/badge/Dificuldade-M%C3%A9dia-yellow)
