# Fase 5 — Plano de Implementação

> Documento de planejamento. **Nenhum código foi alterado.** Lista item a item o que falta em cada página, com base nos wireframes homologados, para elevar a aderência geral do projeto acima de 90%. Aguardando aprovação antes de qualquer alteração.

---

## 1. PÁGINA IMÓVEIS — Formulário (`imoveis.html`)

Wireframe de origem: `audit/wireframes_homologados/imoveis/image10.png` (bloco "Dados do imóvel").

| Item | Campo | Trecho visual correspondente | Local exato de implementação | Impacto desktop | Impacto mobile |
|---|---|---|---|---|---|
| IM4 | Campo **"Bairro / Região"** | Campo de input ao lado de "Endereço completo", coluna "Dados do imóvel" | `imoveis.html`, dentro de `.form-grid` (formulário, `id="formulario"`), novo `.form-field` inserido imediatamente após o campo "Endereço do imóvel"; o campo "Endereço do imóvel" deixa de ter a classe `.full` para formar par com "Bairro/Região" na mesma linha (igual ao wireframe) | Linha do formulário passa a ter 2 colunas (Endereço + Bairro/Região) em vez de 1 coluna cheia | `.form-grid` já colapsa para 1 coluna em telas ≤700px (regra existente em `styles.css:490`); os dois campos empilham verticalmente, sem necessidade de novo CSS |
| IM5 | Campo **"Tipo de imóvel"** (select, obrigatório) | Campo "Tipo de imóvel ▾" marcado em vermelho como obrigatório, ao lado de "Área total (m²)" | Novo `.form-field` com `<select required>`, inserido logo após o campo "Metragem aproximada (m²)" existente, formando par na mesma linha | Forma par com o campo de metragem já existente (2 colunas) | Empilha abaixo da metragem em telas pequenas |
| IM6 | Campo **"Valor pretendido (R$)"** | Campo de input "Valor pretendido (R$)" | Novo `.form-field` com `<input type="text">`, inserido após o novo campo "Tipo de imóvel" | Forma par com "Situação atual" (IM7) na mesma linha | Empilha normalmente |
| IM7 | Campo **"Situação atual"** (select, obrigatório) | Campo "Situação atual ▾" marcado em vermelho como obrigatório, ao lado de "Valor pretendido" | Novo `.form-field` com `<select required>` (opções: Disponível / Ocupado / Em reforma — placeholder de opções), inserido junto a IM6 | Par com IM6 | Empilha normalmente |
| IM8 | **Upload de fotos** (fachada, interior, entorno) | Campo de upload "↑ Fotos — fachada, interior e entorno", linha cheia, abaixo da descrição | Novo `.form-field.full` com `<input type="file" multiple accept="image/*">` e rótulo "Fotos — fachada, interior e entorno", inserido depois do campo "Mensagem" e antes do botão "Enviar indicação" | Ocupa a largura total do formulário (`.full`), abaixo da descrição | Ocupa largura total, sem alteração de comportamento |

**Observação:** o campo "Link Google Maps (opcional)" já existe na implementação atual (`imoveis.html:131`) e não consta na lista aprovada de itens desta fase — não será tocado. O componente "Possui estacionamento" (select) já existente também é mantido sem alteração.

**Itens não tocados nesta página:** IM1, IM2 (interpretativos, fora do escopo da Fase 5), IM3 e IM9 (já implementados na Fase 3).

---

## 2. PÁGINA FORNECEDORES — Formulário (`fornecedores.html`)

Wireframe de origem: `audit/wireframes_homologados/fornecedores/image9.png` (blocos "Dados da empresa" e "Produtos e operação").

| Item | Campo | Trecho visual correspondente | Local exato de implementação | Impacto desktop | Impacto mobile |
|---|---|---|---|---|---|
| FO4 | Campo **"Cargo"** | Campo de input "Cargo", ao lado de "Nome do responsável" | Novo `.form-field`, inserido imediatamente após o campo "Responsável" existente — formam par na mesma linha | Par com "Responsável" | Empilha normalmente |
| FO5 | Campos **"Cidade sede" / "Estado sede"** | Campos "Cidade sede" e "Estado sede ▾", linha própria | Dois novos `.form-field` (input + select com as 14 siglas já usadas em outros formulários do site), inseridos após o campo "E-mail" e antes de "Categoria" | Par lado a lado (Cidade sede + Estado sede) | Empilham normalmente |
| FO6 | Campo **"Site ou portfólio (opcional)"** | Campo de input "Site ou portfólio de produtos (opcional)", linha cheia | Novo `.form-field.full` com `<input type="url">`, inserido após "Estado sede" e antes de "Categoria" | Largura total | Largura total |
| FO7 | Campo **"Capacidade mensal aproximada"** | Campo de input "Capacidade mensal aproximada" | Novo `.form-field`, inserido após o campo "Categoria" existente | Par com o próximo novo campo (FO8) | Empilha normalmente |
| FO8 | Campo **"Estado(s) de atuação / cobertura logística"** (select) | Campo "Estado(s) de atuação / cobertura logística ▾" (tag "novo") | Novo `.form-field` com `<select multiple>` (siglas de estado), inserido junto a FO7 | Par com FO7 | Empilha normalmente |
| FO9 | **Upload de catálogo/apresentação** (PDF, opcional) | Campo de upload "↑ Catálogo, apresentação ou tabela comercial (PDF, opcional)", linha cheia | Novo `.form-field.full` com `<input type="file" accept=".pdf">`, inserido após o campo "Mensagem" e antes do botão "Enviar cadastro" | Largura total | Largura total |

**Itens não tocados nesta página:** FO1 (interpretativo, fora do escopo), FO2 (já aderente), FO3 e FO10 (já implementados na Fase 3).

---

## 3. PÁGINA EXPANSÃO — Revisão Integral (`expansao.html`)

Wireframe de origem (versão homologada v2): `audit/wireframes_homologados/expansao/image6.png` a `image12.png`.

### 3.1 Pilares — "Modelo que Sustenta a Expansão" (EX3)

| Item | Divergência | Trecho visual | Local exato | Impacto desktop | Impacto mobile |
|---|---|---|---|---|---|
| EX3 | Seção tem 3 cards genéricos (Padronização / Critérios claros / Crescimento sustentável); wireframe define **4 pilares com indicador numérico na base**: Varejo popular (+100 lojas), Gestão padronizada (14 estados), Compras em escala (+10 anos), Expansão estruturada (Crescimento) | `expansao/image7.png`, bloco "SEÇÃO 3 — MODELO QUE SUSTENTA A EXPANSÃO" | `expansao.html`, seção "Modelo que Sustenta a Expansão" — grid muda de `.grid-3` para `.grid-4`; os 3 cards atuais são substituídos pelos 4 cards do wireframe (textos e indicador numérico na base, reaproveitando o padrão de "Como Operamos" da Home/Quem Somos) | Grid passa de 3 para 4 colunas | `.grid-4` já colapsa em coluna única em mobile (padrão existente em `styles.css`) |

### 3.2 "O que é o Projeto de Expansão" (EX5)

| Item | Divergência | Trecho visual | Local exato | Impacto desktop | Impacto mobile |
|---|---|---|---|---|---|
| EX5 | Seção atual é um bloco de texto livre (2 colunas: texto + imagem); wireframe define **3 cards estruturados**: Investidores e parceiros (tag "Oportunidade de participação"), Proprietários de imóveis (tag "Parceria imobiliária"), Empreendedores e operadores (tag "Operação de unidades") | `expansao/image8.png`, bloco "SEÇÃO 6 — O QUE É O PROJETO DE EXPANSÃO" | `expansao.html`, seção "O que é o Projeto de Expansão" — o bloco atual de texto+imagem é substituído por `.grid.grid-3` com 3 `.card`, cada um com `.badge`/tag, reaproveitando o padrão de cards já usado em outras seções do site | Bloco de 2 colunas (texto+imagem) é substituído por grid de 3 colunas | Grid de 3 colunas colapsa para 1 coluna em mobile |

### 3.3 CTA para a Landing de Expansão

| Item | Divergência | Trecho visual | Local exato | Impacto desktop | Impacto mobile |
|---|---|---|---|---|---|
| EX-CTA1 | CTA final atual (`cta-final`) não tem os 3 bullets de prova social presentes no wireframe ("+100 lojas em operação em 14 estados brasileiros", "Modelo validado ao longo de mais de uma década", "Expansão contínua com critérios estruturados de seleção") | `expansao/image9.png`, bloco "SEÇÃO 7 — CTA PARA A LANDING" | `expansao.html`, seção `.cta-final` — adicionar lista de 3 bullets entre o parágrafo e o botão, reaproveitando o padrão de lista já usado em "O que analisamos" (ícone `✓`) | Lista de 3 itens acrescentada dentro do bloco já existente | Lista empilha normalmente dentro do bloco |

### 3.4 CTA por Perfil (EX6)

| Item | Divergência | Trecho visual | Local exato | Impacto desktop | Impacto mobile |
|---|---|---|---|---|---|
| EX6 | Grid de CTA por perfil atual tem os cards Imóveis / Fornecedores / Trabalhe Conosco / **Contato**; wireframe define Imóveis / Fornecedores / Trabalhe Conosco / **Investidores e Parceiros** (o card "Contato" não existe no wireframe desta página) | `expansao/image9.png`, bloco "SEÇÃO 8 — CTA POR PERFIL — Outros Relacionamentos" | `expansao.html`, seção `.cta-perfil-grid` final — o card "Contato" é substituído pelo card "Investidores e Parceiros" (badge "Investidor", texto "Quer participar financeiramente ou como parceiro de negócio?", link para `contato.html` como canal de investidores, já que não há página própria) | Card substituído na mesma posição do grid de 4 colunas | Mesma substituição, grid já responsivo |

### 3.5 Hero — itens identificados na revisão integral (achado adicional, fora da lista original)

| Item | Divergência | Trecho visual | Observação |
|---|---|---|---|
| EX-HERO1 | Hero atual tem 1 CTA e nenhuma barra de indicadores; wireframe define **2 CTAs** ("Conhecer o Projeto de Expansão" + "Como a expansão acontece ↓") e **4 indicadores** (+100 lojas, 14 estados, +10 anos, Expansão contínua) dentro do próprio hero | `expansao/image6.png`, "SEÇÃO 1 — HERO" | Acrescentar 2º botão (ancora para a seção "Como a Expansão Acontece") e uma barra de 4 indicadores dentro do hero, reaproveitando o padrão `.stats-bar` já usado no rodapé. **Este item não estava na lista original de divergências objetivas (EX1 era classificado apenas como interpretativo, referente ao overlay) — está sendo reportado aqui como achado da revisão integral solicitada, para sua decisão.** |

### 3.6 Itens explicitamente fora do escopo desta fase

- **EX1** (overlay do hero) e **EX2** (títulos das 7 etapas) e **EX4** (nomes dos critérios) são divergências **interpretativas** (diferença de redação/estética, não de estrutura ausente) — não serão alterados nesta fase, conforme distinção já estabelecida em `VALIDACAO_DAS_DIVERGENCIAS.md`. Caso deseje que also sejam ajustados, preciso de aprovação específica, já que envolvem reescrita de texto, não preenchimento de lacuna estrutural.
- A estrutura das 7 etapas ("Como a Expansão Acontece") **já existe** na implementação atual com 7 passos — a única divergência é de **nomenclatura/texto** de cada etapa (interpretativa), não de quantidade ou de seção ausente.

---

## Resumo de impacto por arquivo

| Arquivo | Itens implementados nesta fase | Tipo de alteração |
|---|---|---|
| `imoveis.html` | IM4, IM5, IM6, IM7, IM8 | Apenas adição de campos ao formulário existente (`.form-grid` / `.form-field`) |
| `fornecedores.html` | FO4, FO5, FO6, FO7, FO8, FO9 | Apenas adição de campos ao formulário existente (`.form-grid` / `.form-field`) |
| `expansao.html` | EX3, EX5, EX6, EX-CTA1 (e EX-HERO1, mediante aprovação) | Substituição de conteúdo dentro de seções já existentes — nenhuma seção nova é criada, nenhuma seção é removida |
| `styles.css` | Nenhuma alteração prevista — todos os componentes necessários (`.form-field`, `.grid-4`, `.card`, `.badge`, `.stats-bar`, ícone `✓`) já existem | — |

## Páginas explicitamente não tocadas nesta fase

Home, Quem Somos, Trabalhe Conosco, Contato, Presença Nacional — nenhuma alteração prevista ou realizada.

---

**Aguardando aprovação para iniciar a implementação. Nenhum código foi alterado até este ponto.**
