# 🚀 CodigoBase - Cypress + Cucumber + Allure

Base de automação de testes E2E utilizando Cypress, Cucumber (BDD) e Allure Report, preparada para escalabilidade e integração com pipelines CI/CD.

---

Como iniciar um novo projeto de automação:

1. Acessar o template CodigoBase
2. Clicar em "Use this template"
3. Criar novo repositório
4. Clonar o novo repositório
5. Rodar npm install
6. Executar cypress open



---

## 📦 Tecnologias utilizadas

- 🧪 Cypress 15
- 🥒 Cucumber (BDD) - @badeball/cypress-cucumber-preprocessor
- ⚡ Esbuild Preprocessor - @bahmutov/cypress-esbuild-preprocessor
- 📊 Allure Report - allure-cypress
- 🔁 Integração com CI/CD (Jenkins-ready)

---

## 📦 Instalação

Clone o repositório:

git clone https://github.com/samuel-delta/CodigoBase.git
cd CodigoBase

Instale as dependências:

npm install

---

## ▶️ Execução dos testes

### Interface gráfica (modo interativo)

npx cypress open

### Execução em modo headless

npx cypress run

---

## 🥒 Execução com Cucumber (BDD)

Os cenários estão localizados em:

cypress/e2e/features/

Exemplo:

Funcionalidade: Login

Cenário: Login com sucesso
  Dado que eu acesso a página de login
  Quando eu informo usuário e senha válidos
  Então o sistema deve permitir o acesso

---

## 📊 Relatório Allure

Após executar os testes:

Gerar relatório:

npx allure generate allure-results --clean -o allure-report

Abrir relatório:

npx allure open allure-report

---

## 📁 Estrutura do Projeto

cypress/
├── e2e/
│   ├── features/
│   │   ├── login.feature
│   │   └── peticionamento.feature
│   │
│   └── step_definitions/
│       ├── login/
│       │   └── login.steps.js
│       └── peticionamento/
│           └── peticionamento.steps.js
│
├── fixtures/
├── support/
│   ├── commands.js
│   └── e2e.js
│
├── screenshots/
└── videos/

allure-results/
allure-report/

cypress.config.js
package.json

---

## ⚙️ Configuração do Allure

Arquivo:

cypress/support/e2e.js

Conteúdo:

require("allure-cypress");

---

## ⚙️ Configuração do Cucumber

Arquivo:

cypress.config.js

Responsável por:

- Configurar o preprocessor do Cucumber
- Integrar com esbuild
- Integrar com Allure

---

## 🧠 Boas práticas adotadas

- Organização por feature (domínio)
- Step definitions separadas por funcionalidade
- Estrutura escalável para múltiplos projetos
- Uso de BDD para clareza de requisitos
- Preparado para execução em pipelines CI/CD
- Separação de responsabilidades (feature vs steps)

---

## 🚀 Integração com CI/CD (Jenkins)

Este projeto está preparado para:

- Execução automatizada via Jenkins
- Geração de relatório Allure após execução
- Possível exportação para PDF
- Execução por suíte (ex: login, peticionamento)

---

## 📌 Pré-requisitos

- Node.js versão 18 ou superior
- npm instalado

Opcional (Allure CLI):

npm install -g allure-commandline

---

## ⚠️ Observações importantes

Não subir pastas como:

- node_modules
- allure-results
- allure-report
- screenshots
- videos

Utilize .gitignore corretamente

---

## 👨‍💻 Autor

Samuel Nunes  
QA Engineer | Automação de Testes | CI/CD

---

## ⭐ Objetivo do projeto

Servir como template base reutilizável para automação de testes E2E com Cypress, permitindo padronização, escalabilidade e rápida adoção em novos projetos.

---

## 🔥 Evoluções futuras

- Pipeline Jenkins completa
- Geração automática de PDF
- Integração com e-mail
- Dashboard de testes
- Execução paralela
- Integração com GitHub Actions
