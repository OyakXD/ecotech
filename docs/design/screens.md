# Telas

Especificação das telas do board e das previstas. **Fonte:** [`identity-board.png`](../brand/identity-board.png). Componentes: [`components.md`](./components.md). Tokens: [`/DESIGN.md`](../../DESIGN.md).

Legenda: **[BOARD]** aparece no board; **[PROPOSTA]** não está no board, é sugestão coerente com a marca e deve ser validada pela equipe (escopo funcional ainda **[ABERTO]**, ver [`decisions.md`](../process/decisions.md)). Todos os números e nomes nos exemplos são ilustrativos.

## 1. Cabeçalho da plataforma + banner de abertura [BOARD]

```
┌──────────────────────────────────────────────────────────────┐
│ [logo]                        Início  Mapa  Recompensas  (👤) │  navbar branca, 64px
├──────────────────────────────────────────────────────────────┤
│ ░░ foto: cidade com árvores, overlay grafite à esquerda ░░░░ │
│   Juntos por                                       ╱ curva   │
│   uma cidade                                      ╱  de      │
│   mais verde  ← "mais verde" em primary-soft     ╱   folha   │
│   [Encontrar ponto de coleta]  ← botão sobre escuro          │
└──────────────────────────────────────────────────────────────┘
```

- Título Display; um único CTA primário acima da dobra.
- Mobile: foto vira fundo com overlay mais forte; navegação em menu.
- Acessibilidade: contraste do texto sobre foto garantido pelo overlay; `alt` na foto.

## 2. Login [BOARD]

```
        ┌────────────────────────┐
        │        [símbolo]       │  logo vertical, ~96px de largura
        │        EcoTech         │
        │                        │
        │   Bem-vindo de volta!  │  Headline
        │  E-mail   [__________] │
        │  Senha    [__________] │
        │  [        Entrar     ] │  botão primário, largura total
        │      Criar conta       │  link terciário
        └────────────────────────┘   cartão branco, xl, sombra Card, max 400px
```

- Fundo `mint-surface` com curva de folha discreta no canto.
- Erros por campo (texto + ícone), erro geral em `role="alert"`. "Esqueci minha senha" como link. Sem login social até decisão (D-02).
- Estados: padrão, carregando ("Entrando..."), erro de credencial ("E-mail ou senha incorretos. Tente de novo."), conta criada.

## 3. Painel administrativo [BOARD]

```
┌────────────┬─────────────────────────────────────────────────┐
│ [logo]     │  Dashboard                                      │
│ ▣ Dashboard│ ┌──────────────┐ ┌──────────┐ ┌──────────┐      │
│ ◎ Mapa     │ │ ♻ 12.480     │ │ KPI 2    │ │ KPI 3    │      │
│ ☺ Usuários │ │ Pontos       │ │          │ │          │      │
│ ★ Recomp.  │ │ coletados ╱╲╱│ └──────────┘ └──────────┘      │
│ ▤ Relatór. │ └──────────────┘                                │
│            │  [ gráfico de tendência ]  [ tabela recentes ]  │
└────────────┴─────────────────────────────────────────────────┘
```

- Operate: legibilidade, consistência e densidade média acima de expressão. Marca só nos detalhes (logo, verdes, ícones).
- KPI com tendência; gráficos com alternativa em tabela; filtros de período como controle segmentado.
- Itens da navegação: Dashboard, Mapa, Usuários, Recompensas, Relatórios. Conteúdo de cada um além do Dashboard é **[PROPOSTA]**.
- Toda tabela: cabeçalhos com `scope`, ordenação por teclado, estado vazio, paginação, versão empilhada no mobile.

## 4. Cartão de recompensas [BOARD]

Ver "Cartão de recompensa" em `components.md`. Aparece no perfil do cidadão e, em miniatura, no cabeçalho do app (saldo). Também serve de modelo para o cartão impresso/digital institucional.

## 5. Material institucional [BOARD]

Peça de apoio (folheto, slide, post): fundo branco ou `mint-wash`, logo vertical centralizado no topo, mensagem curta ("Uma cidade mais sustentável começa com você."), silhueta de cidade verde em `primary` a ~15% na base. Margens generosas, um só ponto focal. Rodapé de assinatura (ver §8).

## 6. Ícone do app e favicon [BOARD]

`public/brand/icon-app.svg` e `favicon.svg`. Ver guia de marca §3 e §4.

## 7. Mapa de pontos de coleta [PROPOSTA]

Página principal do cidadão. Mapa em tela cheia no desktop com lista lateral; no mobile, mapa com gaveta inferior de lista. Pinos hexagonais. Busca por endereço/CEP, filtros por tipo de material (chips), cartão do ponto (nome, distância, "Aberto agora", materiais aceitos, botão "Como chegar"). Obrigatório: lista como alternativa acessível, estado sem resultados, permissão de localização pedida **com explicação** e opcional (LGPD, D-14).

## 8. Rodapé de assinatura [BOARD]

Faixa grafite/verde escuro com logo horizontal `on-dark`, assinatura "Pequenas atitudes. **Grandes transformações.**" (segunda frase em `primary`) e quatro pilares em linha com ícone: Reciclagem inteligente · Conexão com a cidade · Recompensas sustentáveis · Um futuro mais verde. Em mobile, pilares em grade 2×2.

## 9. Recompensas, Perfil, Parceiros [PROPOSTA]

- **Recompensas:** cartão de saldo no topo; grade de benefícios (parceiro, descrição, custo em pontos, "Resgatar"); estado "pontos insuficientes" mostra quanto falta, sem culpa.
- **Perfil do cidadão:** avatar, nível/selo hexagonal (se houver gamificação, D-04), histórico de descartes.
- **Área do parceiro:** validação de entregas e extrato. Fluxo **[ABERTO]**.

## Checklist antes de dar uma tela como pronta

Ver [`workflow.md`](../process/workflow.md) §6 (definição de pronto de UI).
