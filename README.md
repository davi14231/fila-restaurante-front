<div align="center">

# Fila Restaurante - Frontend

Sistema de gerenciamento de filas para restaurantes com atualizações em tempo real

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)
![React](https://img.shields.io/badge/react-19.2.0-61DAFB?style=for-the-badge&logo=react)
![Vite](https://img.shields.io/badge/vite-7.2.2-646CFF?style=for-the-badge&logo=vite)

</div>

---

## Sobre o Projeto

Sistema completo para gestão de filas em restaurantes. Permite que clientes entrem na fila digitalmente, acompanhem sua posição em tempo real e sejam notificados quando estiver próximo de serem atendidos. Do lado do restaurante, oferece painéis para operadores gerenciarem a fila, dashboard com métricas de atendimento e um painel público para exibição em TVs.

Desenvolvido com React 19, WebSocket para comunicação em tempo real, e interface responsiva com Tailwind CSS.



## Funcionalidades

- **Gestão de Tickets Digital**: Clientes recebem tickets digitais com posição atualizada em tempo real
- **Dashboard Analítico**: Métricas de tempo médio de espera, picos de atendimento e taxa de abandono
- **Múltiplos Perfis**: Interfaces separadas para clientes, operadores, administradores e painel público (TV)
- **Notificações em Tempo Real**: Comunicação via WebSocket para atualizações instantâneas
- **Interface Responsiva**: Adaptada para mobile, tablet e desktop
- **Histórico Completo**: Rastreamento de todos os tickets processados
- **Configurações Personalizadas**: Ajuste de horários, capacidade e regras de fila

---

## Stack Tecnológica

### **Frontend**
![React](https://img.shields.io/badge/React-19.2.0-20232A?style=flat&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-7.2.2-646CFF?style=flat&logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind-3.4.18-38B2AC?style=flat&logo=tailwind-css&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router-7.9.6-CA4245?style=flat&logo=react-router&logoColor=white)

### **Comunicação**
![Axios](https://img.shields.io/badge/Axios-1.13.2-5A29E4?style=flat&logo=axios&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-4.8.1-010101?style=flat&logo=socket.io&logoColor=white)

### **DevOps & Ferramentas**
![ESLint](https://img.shields.io/badge/ESLint-9.39.1-4B32C3?style=flat&logo=eslint&logoColor=white)
![PostCSS](https://img.shields.io/badge/PostCSS-8.5.6-DD3A0A?style=flat&logo=postcss&logoColor=white)
![Vercel](https://img.shields.io/badge/Deploy-Vercel-000000?style=flat&logo=vercel&logoColor=white)

---

## Instalação e Execução

### Pré-requisitos

- Node.js >= 18.x
- npm >= 9.x ou yarn >= 1.22.x
- Git

### Instalação

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/fila-restaurante-front.git
cd fila-restaurante-front
```

2. Instale as dependências:
```bash
npm install
```

3. Configure as variáveis de ambiente:

Crie um arquivo `.env` na raiz do projeto:
```env
VITE_API_URL=http://localhost:3000/api/v1
```

4. Inicie o servidor de desenvolvimento:
```bash
npm run dev
```

5. Acesse a aplicação em `http://localhost:5173`

### Build para Produção

```bash
npm run build
npm run preview
```

### Rodando com Docker

Se você tiver o backend configurado com Docker Compose:
```bash
docker-compose up -d
```

---

## Estrutura do Projeto

```
fila-restaurante-front/
├── public/                  # Arquivos estáticos
├── src/
│   ├── assets/             # Imagens, ícones, fontes
│   ├── components/         # Componentes reutilizáveis
│   │   └── WebSocketStatus.jsx
│   ├── hooks/              # Custom React Hooks
│   │   └── useWebSocket.js  # Hook para conexão WebSocket
│   ├── paginas/            # Páginas/Rotas principais
│   │   ├── EscolhaPerfil.jsx      # Tela inicial (Cliente/Restaurante)
│   │   ├── LoginCliente.jsx       # Login do cliente
│   │   ├── CadastroCliente.jsx    # Cadastro de cliente
│   │   ├── RestaurantesDisponiveis.jsx  # Lista de restaurantes
│   │   ├── EntrarNaFila.jsx       # Cliente entra na fila
│   │   ├── AcompanharFila.jsx     # Cliente acompanha seu ticket
│   │   ├── PerfilCliente.jsx      # Perfil do cliente
│   │   ├── HistoricoClienteTickets.jsx  # Histórico do cliente
│   │   ├── LoginRestaurante.jsx   # Login do restaurante
│   │   ├── CadastroRestaurante.jsx # Cadastro do restaurante
│   │   ├── PainelAdministrativo.jsx  # Painel admin
│   │   ├── PainelOperador.jsx     # Fila ao vivo (operador)
│   │   ├── Gerenciamento.jsx      # Gestão de equipe
│   │   ├── GerenciamentoFilas.jsx # Configuração de filas
│   │   ├── HistoricoTickets.jsx   # Histórico de tickets
│   │   ├── DetalhesTicket.jsx     # Detalhes de um ticket
│   │   ├── PainelPublico.jsx      # Painel público (TV)
│   │   ├── ConfiguracoesRestaurante.jsx
│   │   └── Dashboard.jsx          # Analytics e métricas
│   ├── services/
│   │   └── api.js          # Configuração Axios + endpoints
│   ├── utils/              # Funções utilitárias
│   ├── App.jsx             # Componente raiz + rotas
│   ├── App.css             # Estilos globais
│   ├── main.jsx            # Entry point
│   └── index.css           # Estilos Tailwind
├── .env.example            # Template de variáveis de ambiente
├── eslint.config.js        # Configuração ESLint
├── tailwind.config.js      # Configuração Tailwind
├── vite.config.js          # Configuração Vite
├── vercel.json             # Deploy Vercel
└── package.json
```
