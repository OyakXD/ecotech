# Decisões

Registro único do que está **decidido** e do que está **em aberto**. Agentes: se o seu trabalho depende de um item **[ABERTO]**, não escolha por conta própria. Pare, registre a dependência na tarefa, implemente apenas o que independe da decisão ou proponha a opção recomendada e peça confirmação. Ao decidir algo, mova o item para "Decidido" com data e responsável.

## Decidido

| ID | Decisão | Origem |
|---|---|---|
| C-01 | Plataforma web, repositório Next.js 16.4.6 + React 19.3 + Tailwind 4.3.3 + TypeScript | Código do repositório |
| C-02 | Identidade: nome, símbolo, paleta (6 cores), Inter, assinatura | Board `docs/brand/identity-board.png` |
| C-03 | Quatro públicos: cidadãos, pontos de coleta/parceiros, administradores, empresas patrocinadoras | Responsável do projeto, 2026-11-24 |
| C-04 | Logotipos serão recriados em SVG a partir do board até haver arquivos oficiais | Responsável do projeto, 2026-11-24 |
| C-05 | Esta fase entrega só documentação e assets de marca; nenhum código de produto | Responsável do projeto, 2026-11-24 |

## Em aberto

Marcados com a **opção recomendada** (a menos custosa de reverter) para acelerar a conversa com a equipe.

| ID | Questão | Recomendação provisória | Bloqueia |
|---|---|---|---|
| D-01 | Backend e banco (Next.js full-stack, API separada ou só front com mock?) | Front com dados mock tipados em `src/data/` até decidir; contratos de dados isolados em `src/lib/` | Qualquer persistência |
| D-02 | Autenticação (e-mail/senha, social, telefone?) e papéis (cidadão, parceiro, admin, patrocinador) | Decidir antes da tela de login real; ler `node_modules/next/dist/docs/01-app/02-guides/authentication.md` | Login, painel, área do parceiro |
| D-03 | Provedor de mapa (Leaflet/OSM, MapLibre, Google Maps…) | Aberto/OSM por custo e privacidade | Tela de mapa |
| D-04 | Regras de pontos: conversão material → pontos, validação do descarte, antifraude, níveis/gamificação | Definir com negócio antes de desenhar saldo/extrato | Recompensas, KPIs |
| D-05 | Idiomas (só pt-BR ou mais?) | Só pt-BR; texto já separado de componentes quando simples | i18n |
| D-06 | Modo escuro do produto | Só tema claro no início; marca já tem versões `on-dark` | Tokens |
| D-07 | Cores derivadas (`mint-surface`, `mint-wash`, `border-soft`, `text-muted`, `danger`, `warning`) | Manter como estão em DESIGN.md | Todos os componentes |
| D-08 | Biblioteca de ícones | Lucide (traço arredondado, combina com o board) | Ícones |
| D-09 | Área de respiro e tamanho mínimo do logotipo | Valores propostos no guia de marca | Uso do logo |
| D-10 | Uso de imagem gerada por IA / banco de fotos | Fotografia real licenciada ou própria | Banners, institucional |
| D-11 | **Adaptação do board:** botões com `primary-strong` (#126B4A) em vez do verde vivo do board, por contraste (3,24:1 vs 6,51:1) | Manter a adaptação | Botões, barra lateral |
| D-12 | Vetores oficiais da logo (designer) | Substituir `public/brand/*` mantendo nomes | Marca |
| D-13 | PWA ou app nativo | Web responsivo; PWA depois, guia em `01-app/02-guides/progressive-web-apps.md` | Ícones PNG, offline |
| D-14 | LGPD: base legal, consentimento de localização, retenção, DPO | Pedir consentimento granular; dados mínimos | Mapa, cadastro |
| D-15 | Testes (unitário/e2e) e CI | Vitest + Playwright; CI com lint, tipos e build | Definição de pronto |
| D-16 | Hospedagem/deploy | Aberto; guias em `01-app/02-guides/deploying-to-platforms.md` | Release |
