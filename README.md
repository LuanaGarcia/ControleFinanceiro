# Sistema de Controle Financeiro

## 📌 Introdução

O **Sistema de Controle Financeiro** é uma solução multiplataforma desenvolvida para ajudar os usuários a gerenciar suas finanças pessoais de forma eficiente e intuitiva. O sistema oferece funcionalidades para registro de transações, criação de orçamentos e análise de dados financeiros através de dashboards interativos.

### 🎯 Objetivo Geral

Desenvolver um sistema acessível e interativo para gerenciamento financeiro pessoal, com suporte para operações offline e sincronização online.

### 📝 Justificativa

A desorganização financeira é um problema comum enfrentado por muitas pessoas. Este sistema visa fornecer uma ferramenta prática que ajude os usuários a entender e organizar suas finanças, promovendo maior controle e educação financeira.

---

## ⚙️ Funcionalidades do Sistema

✔️ Registro de Transações: Cadastro de receitas e despesas, com categorização.  
✔️ Orçamento Mensal: Planejamento de limites por categoria, com alertas de gastos.  
✔️ Dashboards Interativos: Visualização gráfica de receitas, despesas e comparações de orçamento.  
✔️ Sincronização Offline/Online: Acesso e registro de dados sem conexão com internet.  
✔️ Exportação de Relatórios: Geração de relatórios financeiros em PDF/Excel.  
✔️ Configurações Personalizadas: Gerenciamento de conta do usuário e preferências.  

---

## 🛠 Tecnologias Utilizadas

### **Frontend**
🚀 **React.js**: Desenvolvimento web.  
📱 **React Native**: Desenvolvimento mobile.  

### **Backend**
🌐 **Node.js + Express**: Construção de APIs RESTful.  
🔑 **JWT**: Implementação de autenticação segura.  

### **Banco de Dados**
🔥 **Firebase Firestore**: Banco de dados NoSQL gerenciado pelo Firebase, permitindo sincronização em tempo real e armazenamento na nuvem.  
🔐 **Firebase Authentication**: Para autenticação de usuários.  
📂 **Firebase Storage**: Armazenamento de arquivos como relatórios exportados.  

### **Ferramentas Auxiliares**
🎨 **Figma**: Prototipação de interface.  
🐳 **Docker**: Containerização do ambiente.  
🔍 **Sentry/New Relic**: Monitoramento de erros e desempenho.  
🛠 **Git/GitHub**: Controle de versão.  

---

## 🔍 Análise de Requisitos

### **Requisitos Funcionais**
1️⃣ Cadastro de usuários com autenticação segura via Firebase Authentication.  
2️⃣ Registro de transações (receitas e despesas) armazenadas no Firestore.  
3️⃣ Planejamento e acompanhamento de orçamentos por categoria.  
4️⃣ Visualização de dashboards interativos.  
5️⃣ Sincronização de dados entre dispositivos via Firebase Firestore.  
6️⃣ Exportação de relatórios financeiros armazenados no Firebase Storage.  

### **Requisitos Não Funcionais**
✔️ O sistema deve ser responsivo para dispositivos móveis e desktops.  
✔️ Deve suportar operação offline e sincronização automática.  
✔️ Garantia de segurança dos dados utilizando Firebase Security Rules e conexões HTTPS.  
✔️ A interface deve ser intuitiva e rápida, com tempo de resposta inferior a 2 segundos.  

---

## 📊 Diagramação

### **5.1 Diagrama de Caso de Uso**

- **Atores**:  
  - 👤 **Usuário**: Realiza registros e acompanha os dados financeiros.  
  - 🔥 **Firebase Backend**: Processa e armazena as informações.  

- **Principais Casos de Uso**:  
  - 📝 Registrar transações (receitas e despesas).  
  - 📊 Criar orçamentos mensais.  
  - 📈 Visualizar dashboards interativos.  
  - 📄 Exportar relatórios financeiros.  
  - 🔄 Sincronizar dados offline-online.  

### **5.2 Estrutura do Firestore**

- **Coleções e Documentos**:  
  - 📌 **users** (Armazena informações dos usuários)  
  - 📌 **transactions** (Subcoleção dentro de cada usuário)  
  - 📌 **budgets** (Armazena os orçamentos mensais por usuário)  

### **5.3 Fluxo de Dados**

1️⃣ **Fluxo de Registro de Transações**:  
   - O usuário insere os dados no frontend.  
   - O frontend envia os dados para o Firestore.  
   - O Firestore armazena os dados na subcoleção `transactions` dentro do usuário.  
   - O frontend recebe a confirmação e atualiza os dashboards.  

2️⃣ **Fluxo de Comparação Orçamento x Gasto**:  
   - O usuário solicita o comparativo de orçamento no frontend.  
   - O frontend busca dados da coleção `budgets` e da subcoleção `transactions`.  
   - O Firestore retorna os valores gastos por categoria.  
   - O frontend exibe os resultados em gráficos interativos.  

---

## ⚙️ Configuração do Ambiente

```markdown
### **Requisitos**
💻 Node.js e npm instalados.  
🔥 Firebase CLI configurado.  
📂 Repositório clonado do GitHub.  

### **Passos**
1️⃣ Instale as dependências do backend com `npm install`.  
2️⃣ Configure o Firebase executando:  
   ```bash
   firebase login
   firebase init
   ```
3️⃣ Inicie o frontend com `npm start` (ou usando Expo para mobile).  
4️⃣ Configure variáveis de ambiente usando um arquivo `.env` para armazenar as chaves do Firebase.  
```

---

## 🧪 Testes

### **Testes Unitários**
✔️ Testar integração do Firestore com operações CRUD.  
✔️ Validar autenticação de usuários.  

### **Testes Funcionais**
✔️ Garantir que o fluxo de login, registro de transações e dashboards funcione conforme esperado.  

### **Testes de Usabilidade**
✔️ Obter feedback de usuários reais para melhorias na interface.  

---

## 🚀 Deploy

### **Passos**:
1️⃣ **Backend**: Firebase Functions ou hospedagem no Firebase Hosting.  
2️⃣ **Frontend**: Hospedar no Netlify ou Vercel.  
3️⃣ **Mobile**: Publicar na Google Play e App Store.  

---

## 📡 Monitoramento

📊 **Firebase Analytics**: Para monitorar eventos no app.  
🛠 **Sentry**: Para rastreamento de erros.  
📈 **New Relic**: Para métricas de desempenho do sistema.  

---

Esse documento atualizado reflete o uso do Firebase ao invés do SQLite. Se precisar de mais alguma modificação, é só avisar! 🚀



