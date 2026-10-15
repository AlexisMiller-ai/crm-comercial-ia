# CRM Comercial com IA

> Vitrine de um sistema em produção na **Exclusive Beauty** (Recife, PE). O código é privado, da empresa. Aqui estão o que o sistema faz, como foi construído e as telas, com os dados ocultos.

O time de vendas atendia clientes pelo WhatsApp do celular, controlava leads em planilha e não tinha como saber quem precisava ser recontatado para recompra. Este CRM juntou tudo em um lugar: a conversa, o lead, a vendedora responsável e o histórico de compras. Hoje a equipe de vendas usa todos os dias.

<p>
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" />
  <img src="https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/WhatsApp_(Evolution_API)-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" />
  <img src="https://img.shields.io/badge/Claude_AI-D97757?style=for-the-badge&logo=anthropic&logoColor=white" />
</p>

## O que o sistema faz

- **Atendimento pelo WhatsApp dentro do CRM** — inbox no estilo WhatsApp Web, com mídia, áudio, figurinhas, citação, reação e atribuição da conversa à vendedora. Cada conversa é vinculada automaticamente ao lead certo.
- **Agentes de IA no atendimento** — respondem clientes automaticamente e ajudam a equipe no dia a dia.
- **Funil de vendas em kanban** — arrastar e soltar entre etapas, três visualizações e qualificação de leads.
- **Leads, contatos e empresas** — cadastro completo, filtros, tags, pontuação de lead e origem de cada lead.
- **Carteira de recompra** — carteira por vendedora, com metas e recálculo automático de quem está na hora de comprar de novo.
- **Produtos e vendas** — catálogo com marcas, itens por venda e histórico de compras de cada cliente.
- **Programa de fidelidade** — regras, prêmios, pontos e resgates.
- **Dashboard** — KPIs e métricas de vendas em tempo real.

## Como foi construído

- **Frontend** em React + TypeScript + Tailwind, com componentes shadcn/ui, gráficos em Recharts e drag-and-drop com dnd-kit.
- **Backend serverless** no Supabase: PostgreSQL, autenticação, Realtime para as conversas chegarem na hora, e Edge Functions para as integrações.
- **WhatsApp** integrado via webhooks da Evolution API: mensagens entram em tempo real e são ligadas ao lead e à vendedora.
- **IA** com Claude (Anthropic), chamada pelas Edge Functions. As chaves ficam só no servidor e nunca chegam ao navegador.
- **Segurança** com Row Level Security no banco: cada usuário só acessa o que é da sua organização e do seu perfil.

## Telas

> Os dados de clientes e da equipe foram ocultados.

<!-- Adicione os prints na pasta screenshots/ e descomente as linhas abaixo -->
<!--
<img src="screenshots/atendimento.png" width="100%" />
<img src="screenshots/pipeline.png" width="100%" />
<img src="screenshots/dashboard.png" width="100%" />
-->

---

Desenvolvido por [Alexis Prado](https://github.com/AlexisMiller-ai).
