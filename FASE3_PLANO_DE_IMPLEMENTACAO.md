# Fase 3 — Plano de Implementação

> Documento de planejamento. Nenhum código foi alterado. Aguardando aprovação explícita antes de qualquer edição de HTML/CSS.

## Escopo aprovado

Apenas as 15 divergências objetivas abaixo. Nada além disso será tocado: sem overlays de hero, sem alteração de redação/nomenclatura/ordem de campos, sem breadcrumb em Quem Somos, sem ajuste de TC4, sem qualquer item de Expansão, sem alteração da seção "Relacionamentos Estratégicos" (3 cards) já existente na Home (H7), sem campos extras em Imóveis/Fornecedores além dos listados.

Princípio geral de implementação: reutilizar componentes CSS já existentes em `styles.css` (`.gallery`, `.timeline`, `.map-wrap`/`.map-placeholder`, `.stats-bar`, `.cta-perfil-grid`, `.contato-layout`, `.sidebar-card`, `.card`, `.grid`) — nenhuma classe nova de layout global será criada; no máximo, pequenas classes auxiliares de escopo local (ex.: `.checklist-item`) se necessário.

---

## 1. HOME (`index.html`)

### H2 — Operação Real (galeria fotográfica)
- **Inserir**: nova seção `<section class="section-alt">` logo após a seção "QUEM SOMOS (resumo)" (atual linhas 51-66) e antes da seção "PRESENÇA NACIONAL (resumo)" (atual linha 69).
- **Conteúdo**: título "Operação Real" + `<div class="gallery">` com 7 `.gallery-item` (Fachada, Clientes, Loja, Inauguração, Produtos, Equipe, Interior de loja), todos com `<span class="placeholder-tag">placeholder</span>`.
- **Componentes reutilizados**: `.section-alt`, `.section-head`, `.section-eyebrow`, `.gallery`, `.gallery-item`, `.placeholder-tag` (idênticos aos já usados em `quem-somos.html` "Galeria Institucional").

### H3 — Presença Nacional (mapa + 14 estados)
- **Alterar**: a seção "PRESENÇA NACIONAL (resumo)" já existente (linhas 69-85) será **ampliada** (não substituída) — mantém o `stats-bar` atual e adiciona, entre o `section-head` e o `stats-bar`, um bloco de mapa + grid de estados.
- **Conteúdo adicionado**: `.map-wrap` com `.map-placeholder` + grid com as 14 siglas (BA, CE, GO, MA, MG, MS, MT, PA, PE, PI, PR, RO, SP, TO).
- **Componentes reutilizados**: `.map-wrap`, `.map-placeholder` (já existem em `styles.css`, usados em `presenca-nacional.html`), `.grid grid-4` ou similar para as siglas.

### H4 — Trajetória de Crescimento (timeline)
- **Inserir**: nova seção `<section class="section-tinted">` entre a seção "PRESENÇA NACIONAL (resumo)" (ampliada acima) e a seção "PROJETO DE EXPANSÃO" (linha 88).
- **Conteúdo**: título "Trajetória de Crescimento" + `<ul class="timeline">` com 4 `.timeline-item` (Fundação, Expansão regional, Presença nacional, 100 lojas / Expansão contínua).
- **Componentes reutilizados**: `.timeline`, `.timeline-item`, `.timeline-year` (idênticos ao componente já usado em "Linha do Tempo" de `quem-somos.html`).

### H6 — Como Operamos (4 pilares)
- **Inserir**: nova seção `<section class="section-alt">` entre a seção "PROJETO DE EXPANSÃO" (linha 88-100) e a seção "RELACIONAMENTOS ESTRATÉGICOS" (linha 103) — **sem tocar nesta última (H7, fora de escopo)**.
- **Conteúdo**: título "Como Operamos" + `<div class="grid grid-4">` com 4 `.card` (Varejo popular, Gestão padronizada, Compras em escala, Expansão contínua), cada um com um mini-indicador na base usando `.stat-num`/`.stat-label` dentro do card.
- **Componentes reutilizados**: `.section-alt`, `.grid grid-4`, `.card`, `.stat-num`, `.stat-label`.

### H8 — Formulário de contato rápido
- **Inserir**: nova seção `<section class="section-tinted">` entre a seção "CTA FINAL" (linha 133-144) e o fechamento de `</main>` (linha 145) — ou seja, como última seção do `<main>`, antes do footer.
- **Conteúdo**: título "Fale rapidamente com a gente" + `.form-card` com `.form-grid` contendo 5 campos: Nome, E-mail, Telefone, Assunto (select categorizado), Mensagem; botão `btn btn-primary`; `.form-note` de protótipo; `.form-success`.
- **Componentes reutilizados**: `.form-card`, `.form-grid`, `.form-field`, `.form-note`, `.form-success` (idênticos ao formulário já usado em `contato.html`/`imoveis.html`/`fornecedores.html`). Atributo `data-prototype-form` reaproveitado para manter o comportamento já existente em `script.js`.

---

## 2. QUEM SOMOS (`quem-somos.html`)

### QS2 — Como Operamos (4 pilares)
- **Inserir**: nova seção `<section class="section-tinted">` (ou `.section-alt`, alternando o padrão de zebra já em uso) entre a seção "Linha do Tempo" (linha 62-87) e a seção "Galeria Institucional" (linha 89-102).
- **Conteúdo**: mesmo padrão de H6 (4 cards: Varejo popular, Gestão padronizada, Compras em escala, Expansão contínua).
- **Componentes reutilizados**: `.grid grid-4`, `.card`, `.stat-num`/`.stat-label`.

### QS3 — Diferenciais Competitivos
- **Inserir**: nova seção entre a seção "Galeria Institucional" (linha 89-102) e a seção "Escala Atual" (linha 104-116).
- **Conteúdo**: título "Diferenciais Competitivos" + `<div class="grid grid-3">` com 3 `.card` (Presença onde outros não chegam / Modelo validado em diversidade regional / Escala com gestão eficiente).
- **Componentes reutilizados**: `.grid grid-3`, `.card`, `.card-icon`.

### QS4 — Presença Nacional (mapa + 14 estados)
- **Inserir**: nova seção entre a seção "Escala Atual" (linha 104-116) e a seção CTA final (linha 118-128).
- **Conteúdo**: mesmo padrão de H3 — `.map-wrap`/`.map-placeholder` + grid das 14 siglas + texto "Presença real. Em todas as regiões do país."
- **Componentes reutilizados**: `.map-wrap`, `.map-placeholder`, `.grid`.

### QS5 — Relacionamentos Estratégicos (CTA final, 4 cards)
- **Alterar**: a seção CTA final atual (linha 118-128, hoje `.cta-final` com 1 botão) será **substituída** por uma seção no padrão `.cta-perfil-grid` com 4 `.cta-perfil` (Expansão — destacado como prioritário, Imóveis, Fornecedores, Trabalhe Conosco), seguindo exatamente o mesmo componente já usado em `imoveis.html` (linhas 132-161) e `fornecedores.html` (linhas 138-167).
- **Justificativa de não-violação do H7**: este CTA é específico de `quem-somos.html` (QS5), distinto da seção "Relacionamentos Estratégicos" da Home (H7), que permanece intocada.
- **Componentes reutilizados**: `.cta-perfil-grid`, `.cta-perfil`, `.badge`, `.btn-primary`.

---

## 3. IMÓVEIS (`imoveis.html`)

### IM3 — Perfil que atende (checklist ✓/✗, 8 itens)
- **Alterar**: a seção "Perfil do Imóvel Desejado" (linhas 62-75, atualmente 4 `.card` genéricos: Localização/Metragem/Estrutura/Documentação) será **substituída** por um checklist com 8 itens em formato positivo/negativo (✓ Térreo com acesso direto, ✓ Área mínima, ✓ Alto fluxo, ✓ Boa visibilidade, ✓ Estacionamento como diferencial, ✓ Localização em região comercial, ✗ Andares superiores sem acesso — não atende, ✗ Regiões com baixo fluxo — não atende).
- **Componentes reutilizados**: `.grid grid-2` (2 colunas: atende / não atende) com `.card` simplificado contendo um ícone ✓/✗ textual — nenhuma classe nova de layout, apenas marcação textual dentro do `.card` já existente.

### IM9 — Sidebar do formulário
- **Alterar**: a estrutura da seção "Formulário" (linhas 92-130) passa a usar o layout de duas colunas `.contato-layout` (mesmo grid `1.6fr 1fr` já usado em `contato.html`, linha 79), envolvendo o `.form-card` existente na coluna esquerda e adicionando uma nova `<aside>` na coluna direita com `.sidebar-card`: "O que analisamos em cada imóvel", "Prazo de retorno", "Dúvidas? canal de imóveis".
- **Componentes reutilizados**: `.contato-layout`, `.sidebar-card` (idênticos a `contato.html` linhas 79-123).

---

## 4. FORNECEDORES (`fornecedores.html`)

### FO3 — Critério documental (4º critério em "Critérios de Homologação")
- **Alterar**: a seção "Critérios de Homologação" (linhas 77-89, atualmente 3 `.card`: Capacidade produtiva / Qualidade do produto / Condições comerciais) recebe um **4º `.card`**: "Regularidade cadastral e documental", e o grid passa de `.grid-3` para `.grid-4`.
- **Componentes reutilizados**: `.grid grid-4`, `.card` (mesmo padrão dos 3 cards existentes).

### FO10 — Sidebar do formulário
- **Alterar**: a estrutura da seção "Formulário" (linhas 106-136) passa a usar `.contato-layout`, com o `.form-card` existente na coluna esquerda e uma nova `<aside>` na coluna direita com `.sidebar-card`: "Categorias com demanda ativa", "O que analisamos", "Prazo de retorno", "Canal de fornecedores".
- **Componentes reutilizados**: `.contato-layout`, `.sidebar-card`.

---

## 5. CONTATO (`contato.html`)

### CO4 — Campo "Empresa / Organização (opcional)"
- **Alterar**: dentro de `.form-grid` do formulário único (linhas 84-98), adicionar um novo `.form-field` "Empresa / Organização (opcional)" — inserido após o campo "Telefone" (linha 87) e antes do campo "Assunto" (linha 88), mantendo o padrão visual de input já existente. (Posicionamento segue a ordem natural do formulário; não há alteração de ordem dos campos já existentes, apenas inserção de um novo campo.)
- **Componentes reutilizados**: `.form-field`, `<input type="text">`.

### CO5 — Campo "Sede (Cidade/Estado)" na sidebar
- **Alterar**: dentro do `.sidebar-card` "Sol Magazine" (linhas 107-113), adicionar uma nova linha `<p>Sede: Cidade/Estado <span class="placeholder-tag">placeholder</span></p>` junto às demais informações institucionais já existentes (Razão social, Endereço, Horário, CNPJ).
- **Componentes reutilizados**: `.sidebar-card`, `.placeholder-tag` (mesmo padrão das linhas vizinhas já existentes).

---

## Resumo de arquivos alterados

| Arquivo | Itens implementados |
|---|---|
| `index.html` | H2, H3, H4, H6, H8 |
| `quem-somos.html` | QS2, QS3, QS4, QS5 |
| `imoveis.html` | IM3, IM9 |
| `fornecedores.html` | FO3, FO10 |
| `contato.html` | CO4, CO5 |

Nenhum outro arquivo (`presenca-nacional.html`, `expansao.html`, `trabalhe-conosco.html`, `styles.css` salvo eventuais pequenos ajustes pontuais de classes auxiliares já catalogadas, `script.js`) será alterado nesta fase.

---

**Aguardando aprovação para iniciar a implementação.**
