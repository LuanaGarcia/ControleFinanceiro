# ControleFinanceiro
Trabalho de conclusão de curso

# Sistema de Controle Financeiro

## 1. Introdução

O **Sistema de Controle Financeiro** é uma solução multiplataforma desenvolvida para ajudar os usuários a gerenciar suas finanças pessoais de forma eficiente e intuitiva. O sistema oferece funcionalidades para registro de transações, criação de orçamentos e análise de dados financeiros através de dashboards interativos.

### Objetivo Geral

Desenvolver um sistema acessível e interativo para gerenciamento financeiro pessoal, com suporte para operações offline e sincronização online.

### Justificativa

A desorganização financeira é um problema comum enfrentado por muitas pessoas. Este sistema visa fornecer uma ferramenta prática que ajude os usuários a entender e organizar suas finanças, promovendo maior controle e educação financeira.

---

## 2. Funcionalidades do Sistema

- **Registro de Transações**: Cadastro de receitas e despesas, com categorização.
- **Orçamento Mensal**: Planejamento de limites por categoria, com alertas de gastos.
- **Dashboards Interativos**: Visualização gráfica de receitas, despesas e comparações de orçamento.
- **Sincronização Offline/Online**: Acesso e registro de dados sem conexão com internet.
- **Exportação de Relatórios**: Geração de relatórios financeiros em PDF/Excel.
- **Configurações Personalizadas**: Gerenciamento de conta do usuário e preferências.

---

## 3. Tecnologias Utilizadas

### Frontend
- **React.js**: Desenvolvimento web.
- **React Native**: Desenvolvimento mobile.

### Backend
- **Node.js + Express**: Construção de APIs RESTful.
- **JWT**: Implementação de autenticação segura.

### Banco de Dados
- **SQLite**: Armazenamento offline.
- **PostgreSQL/MySQL**: Banco de dados online.

### Ferramentas Auxiliares
- **Figma**: Prototipação de interface.
- **Docker**: Containerização do ambiente.
- **Sentry/New Relic**: Monitoramento de erros e desempenho.
- **Git/GitHub**: Controle de versão.

---

## 4. Análise de Requisitos

### Requisitos Funcionais
1. Cadastro de usuários com autenticação segura.
2. Registro de transações (receitas e despesas).
3. Planejamento e acompanhamento de orçamentos por categoria.
4. Visualização de dashboards interativos.
5. Sincronização de dados entre dispositivos.
6. Exportação de relatórios financeiros.

### Requisitos Não Funcionais
1. O sistema deve ser responsivo para dispositivos móveis e desktops.
2. Deve suportar operação offline e sincronização automática.
3. Garantia de segurança dos dados utilizando criptografia AES e conexões HTTPS.
4. A interface deve ser intuitiva e rápida, com tempo de resposta inferior a 2 segundos.

---

## 5. Diagramação

### 5.1 Diagrama de Caso de Uso

- **Atores**:
  - **Usuário**: Realiza registros e acompanha os dados financeiros.
  - **Sistema Backend**: Processa e armazena as informações.

- **Principais Casos de Uso**:
  - Registrar transações (receitas e despesas).
  - Criar orçamentos mensais.
  - Visualizar dashboards interativos.
  - Exportar relatórios financeiros.
  - Sincronizar dados offline-online.

### 5.2 Diagrama de Entidade-Relacionamento (ER)

- **Entidades e Relacionamentos**:
  1. **Usuário**: `id`, `nome`, `email`, `senha`.
  2. **Transação**: `id`, `valor`, `tipo`, `data`, `categoria_id`, `usuario_id`.
  3. **Categoria**: `id`, `nome`.
  4. **Orçamento**: `id`, `mes`, `ano`, `usuario_id`.
  5. **OrçamentoCategoria**: `id`, `orcamento_id`, `categoria_id`, `valor_orcado`, `valor_gasto`.

### 5.3 Diagrama de Sequência

#### Fluxo de Registro de Transações:
1. O usuário insere os dados no frontend.
2. O frontend envia os dados para a API do backend.
3. O backend valida e armazena as informações.
4. O backend retorna uma confirmação ao frontend.
5. O frontend atualiza os dashboards em tempo real.

#### Fluxo de Comparação Orçamento x Gasto:
1. O usuário solicita o comparativo de orçamento no frontend.
2. O frontend envia uma requisição ao backend.
3. O backend calcula os valores gastos e planeja a comparação.
4. O backend retorna os dados processados ao frontend.
5. O frontend exibe os resultados em gráficos interativos.

---

## 6. Detalhamento das Telas

### 6.1 Tela de Login
- **Campos**:
  - E-mail.
  - Senha.
- **Botões**:
  - Login.
  - Cadastro.
  - Recuperar senha.
- **Validações**: Mensagens de erro para credenciais inválidas.

### 6.2 Tela de Cadastro de Transações
- **Campos**:
  - Valor (com validação monetária).
  - Categoria (menu suspenso).
  - Tipo (Receita ou Despesa).
  - Data (calendário interativo).
  - Descrição (campo de texto).
- **Botão**: Salvar transação.

### 6.3 Tela de Orçamento Mensal
- **Campos**:
  - Categoria.
  - Limite planejado por categoria.
  - Gasto total por categoria (calculado automaticamente).
- **Indicadores**: Barra de progresso mostrando a porcentagem gasta.
- **Botões**:
  - Adicionar categoria.
  - Editar orçamento.

### 6.4 Tela de Dashboard
- **Componentes**:
  - Gráfico de Pizza: Distribuição de despesas por categoria.
  - Gráfico de Barras: Comparativo de receitas e despesas.
  - Indicadores: Saldo atual e alertas de orçamento.
- **Filtros**:
  - Período (mensal, trimestral, anual).
  - Categorias.

### 6.5 Tela de Configurações do Usuário
- **Opções**:
  - Alterar e-mail e senha.
  - Configurar notificações.
  - Exportar relatórios em PDF ou Excel.
  - Logout.

---

## 7. Configuração do Ambiente

### Requisitos:
- Node.js e npm instalados.
- SQLite/MySQL configurados.
- Repositório clonado do GitHub.

### Passos:
1. Instale as dependências do backend com `npm install`.
2. Inicie o backend com `npm start`.
3. Inicie o frontend com `npm start` (ou usando Expo para mobile).
4. Configure variáveis de ambiente usando um arquivo `.env`.

---

## 8. Testes

### Testes Unitários
- Testar APIs no backend para CRUD de transações.
- Validar componentes frontend isoladamente.

### Testes Funcionais
- Garantir que o fluxo de login, registro de transações e dashboards funcione conforme esperado.

### Testes de Usabilidade
- Obter feedback de usuários reais para melhorias na interface.

---

## 9. Deploy

### Passos:
1. **Backend**: Subir para Heroku ou AWS.
2. **Frontend**: Hospedar no Netlify ou Vercel.
3. **Mobile**: Publicar na Google Play e App Store.

---

## 10. Monitoramento

- **Sentry**: Monitoramento de erros.
- **New Relic**: Métricas de desempenho do sistema.

---


