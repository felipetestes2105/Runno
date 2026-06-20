# Runno MVP V1

Runno e um SaaS de organizacao de rotinas com foco em profissionais e operacoes recorrentes.

## Stack

- React + TypeScript + Vite
- Tailwind CSS v4
- Lucide React
- Framer Motion
- Supabase (auth + schema pronto)

## Estrutura

- `src/app/`: telas principais (auth, dashboard, calendario, tarefas, espacos, configuracoes)
- `src/components/layout/`: shell principal, sidebar e header
- `src/components/dashboard/`: widgets independentes
- `src/components/ui/`: componentes base reutilizaveis
- `src/hooks/`: hooks de comando global e estado do app
- `src/lib/`: supabase client e dados mock para bootstrap
- `src/types/`: contratos TypeScript do dominio
- `supabase/schema.sql`: schema completo com RLS

## Rodando localmente

1. Instale dependencias:
   `npm install`
2. Crie `.env` com base em `.env.example`
3. Rode o projeto:
   `npm run dev`

## Supabase

1. Crie projeto no Supabase.
2. Execute `supabase/schema.sql` no SQL Editor.
3. Copie URL e Anon Key para `.env`.
4. A autenticacao ja alterna entre login/signup e modo demo quando variaveis nao existem.

## Deploy na Vercel

1. Suba o repositorio no GitHub.
2. Importe o projeto na Vercel.
3. Configure variaveis:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_ANON_KEY`
4. Build command: `npm run build`
5. Output: `dist`
