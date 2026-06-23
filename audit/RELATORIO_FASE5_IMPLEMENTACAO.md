# Relatório de Implementação — Fase 5

> Implementação restrita aos itens aprovados parcialmente: IM4–IM8, FO4–FO9 e EX3/EX5/EX6. Hero com 2º CTA, hero com barra de indicadores, bullets adicionais no CTA final de Expansão, EX1, EX2 e EX4 **não foram alterados**, conforme aprovação parcial do usuário.

## Itens implementados por página

### `imoveis.html` — Formulário

- **IM4 — Bairro / Região**: novo campo de input inserido ao lado de "Endereço do imóvel" (que deixou de ocupar a linha cheia, formando par na mesma linha, igual ao wireframe).
- **IM5 — Tipo de imóvel**: novo campo `<select required>` com opções (Térreo, Sobreloja, Loja em galeria/shopping, Outro), inserido ao lado de "Metragem aproximada (m²)".
- **IM6 — Valor pretendido (R$)**: novo campo de input, inserido após "Tipo de imóvel".
- **IM7 — Situação atual**: novo campo `<select required>` com opções (Disponível, Ocupado, Em reforma), inserido ao lado de "Valor pretendido (R$)".
- **IM8 — Upload de fotos**: novo campo `<input type="file" multiple accept="image/*">`, rótulo "Fotos — fachada, interior e entorno", inserido após o campo "Mensagem" e antes do botão "Enviar indicação".

### `fornecedores.html` — Formulário

- **FO4 — Cargo**: novo campo de input, inserido ao lado de "Responsável".
- **FO5 — Cidade sede / Estado sede**: dois novos campos (input + select com as 14 siglas padrão do site), inseridos após "E-mail".
- **FO6 — Site ou portfólio (opcional)**: novo campo `<input type="url">` em linha cheia, inserido após "Estado sede".
- **FO7 — Capacidade mensal aproximada**: novo campo de input, inserido após "Categoria".
- **FO8 — Estado(s) de atuação / cobertura logística**: novo campo `<select multiple>` com as 14 siglas, em linha cheia, inserido ao lado de "Capacidade mensal aproximada".
- **FO9 — Upload de catálogo/apresentação**: novo campo `<input type="file" accept="application/pdf">`, em linha cheia, inserido após o campo "Mensagem" e antes do botão "Enviar cadastro".

### `expansao.html` — Revisão parcial aprovada

- **EX3 — Modelo que Sustenta a Expansão**: grid alterado de `.grid-3` (3 cards genéricos) para `.grid-4` (4 pilares: Varejo popular, Gestão padronizada, Compras em escala, Expansão estruturada), cada card com indicador numérico na base (`.stat`/`.stat-num`/`.stat-label`), reaproveitando exatamente o padrão já usado em "Como Operamos" da Home e Quem Somos.
- **EX5 — O que é o Projeto de Expansão**: o bloco de texto livre (2 colunas: texto + imagem-placeholder) foi substituído por `.grid.grid-3` com 3 cards estruturados: Investidores e parceiros (badge "Oportunidade de participação"), Proprietários de imóveis (badge "Parceria imobiliária"), Empreendedores e operadores (badge "Operação de unidades").
- **EX6 — CTA por Perfil**: o card "Contato" (badge "Geral") foi substituído pelo card "Investidores e Parceiros" (badge "Investidor"), mantendo a mesma posição no grid de 4 colunas; os cards Imóveis, Fornecedores e Trabalhe Conosco permanecem inalterados.

## Itens explicitamente NÃO alterados nesta fase (aprovação parcial)

- Hero de Expansão — 2º CTA ("Como a expansão acontece ↓") **não adicionado**.
- Hero de Expansão — barra de 4 indicadores **não adicionada**.
- CTA final ("Quer levar a Sol Magazine para sua região?") — bullets de prova social **não adicionados**.
- **EX1** (overlay do hero) — não alterado.
- **EX2** (títulos das 7 etapas) — não alterado.
- **EX4** (nomes dos critérios de expansão) — não alterado.
- Home, Quem Somos, Trabalhe Conosco, Contato, Presença Nacional — nenhuma alteração.

## Componentes CSS reutilizados (nenhum componente novo criado)

- `.form-grid` / `.form-field` / `.form-field.full` (IM4–IM8, FO4–FO9)
- `.grid.grid-4` / `.card` / `.stat` / `.stat-num` / `.stat-label` (EX3 — mesmo padrão de "Como Operamos")
- `.grid.grid-3` / `.card` / `.badge` (EX5)
- `.cta-perfil-grid` / `.cta-perfil` / `.badge` (EX6)

## Arquivos alterados

1. `imoveis.html`
2. `fornecedores.html`
3. `expansao.html`

Nenhuma alteração em `styles.css`, `script.js`, header, footer ou demais páginas.

## Evidências

Screenshots desktop (1440×900) e mobile (390×844) das 3 páginas alteradas em `audit/screenshots_fase5/`:
`imoveis_desktop.png`, `imoveis_mobile.png`, `fornecedores_desktop.png`, `fornecedores_mobile.png`, `expansao_desktop.png`, `expansao_mobile.png`.
