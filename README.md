# 🏨 Hotel Gestão - Sistema Full-Stack de Gerenciamento Hoteleiro

An aplicação completa (Full-Stack) desenvolvida para otimizar e automatizar a gestão operacional de hotéis. O sistema conta com controle rigoroso de níveis de acesso (RBAC), permitindo que gerentes e recepcionistas desempenhem suas funções em um ambiente seguro, integrado e performático.

---

## 🚀 Desafios Técnicos Superados & Funcionalidades

Neste projeto, o foco foi além do CRUD básico, implementando padrões arquiteturais de mercado:

- **Autenticação e Segurança (JWT):** Fluxo completo de login com senhas criptografadas via `bcrypt` e geração de tokens assinados com tempo de expiração de 8 horas.
- **Controle de Acesso Baseado em Cargos (RBAC):** Desenvolvimento de middlewares customizados no Node.js que barram ou liberam rotas dependendo do nível do usuário (`GERENTE` ou `RECEPCIONISTA`). Por exemplo, a criação de novas unidades/quartos é restrita a gerentes.
- **Consistência de Estado no Front-end:** Gerenciamento centralizado de sessões utilizando o `LocalStorage` do navegador integrado a modais dinâmicos e atualizações automáticas via Axios.
- **Logs de Atividade:** Arquitetura preparada para rastrear qual funcionário executou cada ação no sistema, garantindo auditoria e conformidade.

---

## 🛠️ Tecnologias Utilizadas

### **Front-end**
- **React.js** (com **Vite** para um ecossistema de desenvolvimento ultra rápido)
- **React Router Dom** (Gerenciamento de rotas protegidas)
- **Axios / Fetch API** (Consumo da API REST)
- **Componentização com CSS-in-JS** (Interfaces limpas, responsivas e profissionais)

### **Back-end**
- **Node.js** com **Express**
- **JSON Web Token (JWT)** (Controle de sessão e segurança)
- **Bcrypt** (Criptografia de senhas)

### **Banco de Dados & Ferramentas**
- **MySQL** (Modelagem de dados relacionais para Usuários, Quartos e Logs)
- **Postman** (Testes automatizados de endpoints)
- **Git & GitHub** (Controle de versionamento)

---

## 📐 Estrutura Arquitetural do Back-end

O projeto segue o padrão MVC (Model-View-Controller) simplificado para manter o código limpo e escalável:

```text
├── src/
│   ├── config/          # Conexão com o Banco de Dados (MySQL)
│   ├── controllers/     # Lógica de negócio (authController, roomController)
│   ├── middlewares/     # Interceptadores de segurança (authMiddleware, roomMiddleware)
│   ├── routes/          # Definição dos endpoints (authRoutes, roomRoutes)
│   └── server.js        # Inicialização do servidor Express

💻 Como Executar o Projeto
Pré-requisitos
Você vai precisar do Node.js e de um banco de dados MySQL rodando localmente.

1. Configuração do Back-end
Clone o repositório e navegue até a pasta do servidor.

Instale as dependências:

Bash
npm install
Crie um arquivo .env na raiz do back-end e configure as seguintes variáveis:

Snippet de código
PORT=7070
DB_HOST=localhost
DB_USER=seu_usuario
DB_PASS=sua_senha
DB_NAME=nome_do_banco
JWT_SECRET=sua_chave_mestra_super_secreta
Inicie o servidor:

Bash
npm run dev
2. Configuração do Front-end
Navegue até a pasta do front-end.

Instale as dependências:

Bash
npm install
Inicie a aplicação Vite:

Bash
npm run dev
Abra o navegador no endereço indicado (geralmente http://localhost:5173).

👤 Autor
Desenhado e desenvolvido com 💻 por Guilherme.

Estudante de Desenvolvimento de Sistemas no SENAI Florianópolis.
