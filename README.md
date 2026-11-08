
<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=30&duration=3000&pause=1000&color=00E5FF&center=true&vCenter=true&width=700&lines=F.R.I.D.A.Y.+OS;Modular+AI+Assistant;Python+%7C+Automation+%7C+AI" alt="F.R.I.D.A.Y. Banner" />

<br/>

<h3>🧠 Modular AI Assistant | CLI Engine</h3>

<p>
  <img src="https://img.shields.io/badge/Python-3.12+-00E5FF?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Architecture-Modular-38BDF8?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Tests-Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white"/>
  <img src="https://img.shields.io/badge/Lint-Ruff-D7FF64?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/CI-GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"/>
</p>

</div>

---

## ⚡ Visão Geral do Sistema

A **Sexta-Feira (F.R.I.D.A.Y.)** é uma assistente modular desenvolvida em Python, projetada para centralizar funcionalidades de automação, organização e suporte ao desenvolvimento de software.

Sua arquitetura permite o isolamento de diferentes módulos funcionais, mantendo o desacoplamento entre responsabilidades e facilitando a evolução do projeto.

> 💡 **Conexão de Engenharia:** O projeto aplica conceitos de organização modular, validação, testes automatizados e integração contínua, inspirados nas práticas de qualidade utilizadas no ecossistema Java/Spring e adaptados ao desenvolvimento de soluções com Python e Inteligência Artificial.

---

## 🧭 Painel de Controle de Módulos

### F.R.I.D.A.Y. ENGINE — V1 CLI

Atualmente operando por uma interface de terminal, com utilização de Type Hints e organização modular.

| Módulo | Identificador | Responsabilidade |
|---|---|---|
| 💻 Tech | `TECH_DEVSIM` | Validação de código e simulação de entrevistas |
| 🏢 Productivity | `PRODUCTIVITY` | Organização de tarefas, atas e logs |
| 💰 Financial | `FINANCIAL_QA` | Controle financeiro e projeções básicas |

### 🔍 Detalhamento dos Módulos

#### 💻 Tech Development
Analisador lógico para trechos de código Python, com validações orientadas às diretrizes PEP 8 e simulador de questões técnicas envolvendo algoritmos e desenvolvimento de software.

#### 🏢 Productivity
Módulo destinado à organização de tarefas, relatórios operacionais, atas e registros de progresso, com geração de arquivos estruturados.

#### 💰 Financial Management
Motor de cálculos para controle financeiro pessoal, categorização de receitas e despesas e projeção básica de gastos.

---

## 🎨 Arquitetura e Fluxo de Execução

O diagrama abaixo representa o fluxo de execução da interface CLI e o direcionamento das solicitações para os módulos internos.

```mermaid
flowchart TD
    USER(["Terminal Input"])
    MAIN["src/main.py"]
    CORE["src/core/engenho.py"]

    TECH["TECH_DEVSIM"]
    CORP["PRODUCTIVITY"]
    FIN["FINANCIAL_QA"]

    USER --> MAIN
    MAIN --> CORE

    CORE -->|Opção 1| TECH
    CORE -->|Opção 2| CORP
    CORE -->|Opção 3| FIN

    TECH --> MAIN
    CORP --> MAIN
    FIN --> MAIN

    MAIN --> USER

    classDef core fill:#0b1329,stroke:#00e5ff,color:#ffffff;
    classDef module fill:#001e2b,stroke:#38bdf8,color:#38bdf8;
    class MAIN,CORE core;
    class TECH,CORP,FIN module;
```

---

## ⚙️ Rigor Técnico & Qualidade

- **Type Hints:** utilização de anotações de tipos para melhorar a legibilidade, documentação e análise estática do código.
- **Testes Automatizados:** validação de comportamentos e regras por meio de Pytest.
- **Linting:** utilização do Ruff para análise estática e padronização do código.
- **Continuous Integration:** GitHub Actions executa verificações automatizadas e testes a cada push.
- **Modularidade:** separação entre interface, lógica central e módulos funcionais.

---

## 🏗️ Estrutura do Projeto

```text
sexta-feira/
├── .github/
│   └── workflows/
│       └── ci.yml
├── src/
│   ├── main.py
│   └── core/
│       └── engenho.py
└── tests/
    └── test_agente.py
```

---

## 🔮 Roadmap de Evolução

```mermaid
flowchart LR
    A["STAGE 01<br/>CLI ENGINE<br/>Python + Rules"]
    B["STAGE 02<br/>INTELLIGENT ROUTING<br/>Gemini API"]
    C["STAGE 03<br/>DISTRIBUTED SERVICES<br/>FastAPI + MySQL"]

    A --> B --> C

    classDef current fill:#001e2b,stroke:#00e5ff,color:#00e5ff;
    classDef future fill:#0b1329,stroke:#38bdf8,color:#ffffff;

    class A current;
    class B,C future;
```

<div align="center">

### ⚡ F.R.I.D.A.Y. — Building the Future, One Module at a Time.

</div>

