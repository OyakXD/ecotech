# Roadmap de desenvolvimento (proposta)

Sequência sugerida para iniciar o desenvolvimento. É uma **proposta** derivada do board e do estado do repositório; escopo funcional, prazos e prioridades dependem da equipe (ver [`decisions.md`](./decisions.md)). Cada fase termina com a definição de pronto de [`workflow.md`](./workflow.md) §6.

## Fase 0: Fundação de marca no código

Sem depender de nenhuma decisão aberta. Pode começar já.

- Aplicar tokens do `DESIGN.md` em `src/app/globals.css`; remover o dark mode do template (D-06).
- Trocar Geist por Inter em `src/app/layout.tsx`; `lang="pt-BR"`; metadata EcoTech (título, descrição com a assinatura).
- Favicon, `icon.svg`, `apple-icon.png` a partir de `public/brand/` (comandos no guia de marca §4); remover SVGs do template em `public/`.
- Componente `Logo` (variantes horizontal/vertical/símbolo, claro/escuro/mono) e átomos: Button, Link, Card, Field, Chip, Avatar, estados vazio/erro/esqueleto.
- Página de exemplo interna (`/design` ou Storybook-like, a decidir) com todos os átomos para revisão visual.

**Pronto quando:** `/` mostra a marca correta (sem template), átomos revisados contra `components.md`, lint/tipos/build verdes.

## Fase 1: Shell público e login (UI)

- Navbar da plataforma, rodapé de assinatura, banner de abertura (tela §1 e §8).
- Tela de login e criar conta **somente UI** com validação de formulário e estados (tela §2). Autenticação real depende de D-02.
- Páginas institucionais mínimas (sobre/propósito) com os quatro propósitos.

**Depende de:** nada para a UI; D-02 para ligar a autenticação.

## Fase 2: Mapa de pontos de coleta

- Lista + mapa, busca, filtros, cartão do ponto, permissão de localização (tela §7).
- Dados mock em `src/data/` com o tipo `PontoDeColeta`.

**Depende de:** D-03 (provedor de mapa), D-14 (localização/LGPD). Dados reais dependem de D-01.

## Fase 3: Pontos e recompensas do cidadão

- Cartão de recompensa, saldo, extrato, catálogo e resgate (telas §4 e §9).
- Perfil do cidadão.

**Depende de:** D-04 (regras de pontos) e D-01 (persistência). Sem D-04, entregue só a UI com mock rotulado.

## Fase 4: Painel administrativo

- Shell com barra lateral, Dashboard com KPIs e gráficos, Usuários, Recompensas, Relatórios (tela §3).

**Depende de:** D-01, D-02 (papéis), D-04 (métricas).

## Fase 5: Parceiros e patrocinadores

- Área do parceiro (validação de entregas, extrato) e do patrocinador (benefícios oferecidos).

**Depende de:** D-01, D-02, D-04 e definição de fluxo de negócio (**[ABERTO]**).

## Paralelo e contínuo

- Substituir logotipos recriados pelos oficiais (D-12).
- Testes e CI (D-15) desde a Fase 0 se possível.
- Material institucional impresso/digital (tela §5).
- Auditoria de acessibilidade e performance antes de cada release.
