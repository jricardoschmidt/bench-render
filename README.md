# Gerador de Render — Banco

Ferramenta interna para gerar renders fotorrealistas de bancos a partir de desenhos técnicos e foto de referência.

## Deploy na Vercel (5 minutos)

### 1. Suba o projeto no GitHub
- Acesse github.com → New repository → nome: `bench-render`
- Faça upload de todos estes arquivos (ou use git)

### 2. Importe na Vercel
- Acesse vercel.com → Log in with GitHub
- "Add New Project" → selecione o repositório `bench-render`
- Clique em **Deploy** (sem alterar nada)

### 3. Configure a variável de ambiente
- No projeto Vercel, vá em **Settings → Environment Variables**
- Adicione:
  - **Name:** `REPLICATE_API_TOKEN`
  - **Value:** seu token da Replicate (r8_xxxx...)
- Clique em **Save** e depois em **Redeploy**

### 4. Pronto
A URL gerada pela Vercel (ex: `bench-render.vercel.app`) já funciona.

## Estrutura
```
bench-render/
├── index.html          ← frontend da ferramenta
├── api/
│   └── replicate.js    ← proxy serverless (resolve o CORS)
├── vercel.json         ← config da Vercel
└── package.json
```

## Como usar a ferramenta
1. Anexe os desenhos técnicos (PNG/JPG)
2. Anexe a foto de referência do banco produzido
3. Informe as dimensões em cm
4. Clique em **"1. Analisar imagens com IA"**
5. Clique em **"2. Gerar render"**
