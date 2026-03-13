# VitrineIA — Painel Admin

## Deploy no Vercel

### 1. Criar repositório no GitHub
```bash
git init
git add .
git commit -m "Painel admin VitrineIA"
git branch -M main
git remote add origin https://github.com/SEU-USER/vitrineia-admin.git
git push -u origin main
```

### 2. Conectar no Vercel
- Acesse vercel.com → New Project → Import do GitHub
- Selecione o repositório `vitrineia-admin`
- Framework: Vite
- Clique em Deploy

### 3. Configurar domínio (opcional)
- Vercel → Project Settings → Domains
- Adicionar: admin.vitrineia.com.br
- Apontar DNS no registro.br

### 4. Primeiro acesso
- Abra o painel
- Na tela de configuração, coloque:
  - **Supabase URL**: sua URL do Supabase
  - **Supabase Key**: sua anon key do Supabase
  - **Anthropic Key**: sua API key (só pro módulo IA Analista)
- As credenciais ficam salvas no navegador

## Módulos

- **Dashboard** — KPIs, clientes recentes, pipeline
- **Clientes** — Gerenciar, pausar/ativar, add-ons
- **IA Analista** — Análise de páginas com Claude
- **Financeiro** — MRR, projeção, receita por fonte
- **Pipeline** — Todos os leads do Outscraper

## Nota sobre IA Analista
O módulo IA Analista faz chamadas diretas à API da Anthropic.
Se der erro de CORS, é necessário adicionar um endpoint proxy
no servidor Railway. Falar com Dan para configurar.
