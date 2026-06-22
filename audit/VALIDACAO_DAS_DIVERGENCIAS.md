# Validação das Divergências — Imagem de Referência, Trecho Exato e Classificação

> Este documento percorre cada divergência listada em `AUDITORIA_VISUAL_FINAL.md`, identifica a imagem exata do wireframe usada como evidência, descreve o trecho visual que sustenta a divergência e classifica cada item como:
> - **A) Divergência objetiva** — campo, seção ou card ausente (binário: existe ou não existe).
> - **B) Divergência interpretativa** — texto diferente, overlay, espaçamento, estética (depende de leitura/julgamento).
>
> Nenhuma alteração de código foi feita nesta etapa.

---

## ACHADO TRANSVERSAL — Overlay do Hero

| Imagem de referência | Trecho exato |
|---|---|
| `presenca-nacional/image15.png` | Bloco "Princípio aplicado": *"O hero ocupa 100% da largura, com a metade direita revelando a foto sem esconder legibilidade nem opacidade. (...) a barra de stats com fundo opaco a 62% de opacidade, mantendo a imagem visível ao fundo."* — comparação "Antes × Depois" mostra explicitamente a área direita da imagem **sem véu**. |

**Classificação: B) Divergência interpretativa.**
Justificativa: não é a ausência de um elemento, e sim uma diferença de tratamento visual (gradiente localizado vs. cor sólida uniforme) — depende de leitura de intenção de design, não é um "existe/não existe".

---

## 1. HOME

| # | Divergência | Imagem de referência | Trecho exato | Classificação |
|---|---|---|---|---|
| H1 | Overlay do hero sem gradiente localizado | `home/image1.png` | Hero "HOME REFINADA v2 — Desktop", bloco vermelho-escuro com gradiente decrescente da esquerda (texto) para a direita | B) Interpretativa |
| H2 | Seção "Operação Real" (galeria de 7 células) ausente | `home/image2.png` | Bloco "SEÇÃO 3 — ÂNCORA ESTRATÉGICA — Operação real: grid fotográfico 7 células · fachadas, clientes, inaugurações, equipe, interior" com as 7 caixas: Fachada, Clientes, Loja, Inauguração, Produtos, Equipe, Interior de loja | A) Objetiva (seção inteira ausente) |
| H3 | Seção "Presença Nacional" com mapa + grid de 14 estados ausente | `home/image2.png` | Bloco "SEÇÃO 4 — Presença nacional — mapa + 14 estados em vermelho + CTA para página interna", com `[Mapa — 14 estados em vermelho]` e grid de siglas (BA, CE, GO, MA, MG, MS, MT, PA, PE, PI, PR, RO, SP, TO) | A) Objetiva (seção/elemento ausente) |
| H4 | Seção "Trajetória de Crescimento" (timeline 01→04) ausente | `home/image3.png` | Bloco "TRAJETÓRIA DE CRESCIMENTO — Uma década de expansão estruturada", com os marcos circulares 01 Fundação, 02 Expansão regional, 03 Presença nacional, 04 100 lojas, → Expansão contínua | A) Objetiva (seção ausente) |
| H5 | Seção "Sobre a Sol Magazine" sem pills/mini indicadores | `home/image3.png` | Bloco "SEÇÃO 6 — REFORÇADA — Quem somos: título forte + parágrafo denso + pills + foto + mini indicadores", com as pills `+100 lojas em operação` `14 estados` `+10 anos de atuação` e o card de 3 mini-indicadores ao lado da foto | A) Objetiva (pills e mini-indicadores ausentes como elementos) — *nota: o texto da seção em si existe; o que falta são elementos visuais específicos (pills + mini-indicadores), por isso classificado como objetivo (presença/ausência de elemento), não como diferença de texto* |
| H6 | Seção "Como Operamos" (4 pilares) ausente | `home/image4.png` | Bloco "SEÇÃO 7 — REFORÇADA — Modelo operacional: 4 pilares com indicador operacional na base de cada card", cards Varejo popular / Gestão padronizada / Compras em escala / Expansão contínua, cada um com indicador na base (+100 lojas, 14 estados, +10 anos, Crescimento) | A) Objetiva (seção ausente) |
| H7 | Seção "Oportunidades" com 4 cards (Expansão destacado) trocada por "Relacionamentos Estratégicos" com 3 cards | `home/image4.png` | Bloco "SEÇÃO 8 — ÂNCORA DE CONVERSÃO — Oportunidades por perfil — 4 cards · Expansão com destaque · CTA distinto por público", card "Expansão" com tag `Público prioritário` + Imóveis + Fornecedores + Trabalhe Conosco | A) Objetiva (card "Expansão" e rótulo de seção ausentes/trocados) |
| H8 | Formulário de contato rápido embutido na Home ausente | `home/image5.png` | Bloco "SEÇÃO 9 — Contato rápido — formulário com assunto categorizado · 5 campos": Nome, E-mail, Telefone, Assunto (dropdown), Mensagem + botão "Enviar mensagem" | A) Objetiva (seção/formulário ausente) |
| H9 | Fundo geral da página em tom mais escuro (`#1a0808`) | `home/image1.png` (cabeçalho do documento) | Anotação de fundo escuro no corpo do documento de wireframe, perceptível no contraste das seções "SEÇÃO 1/2" | B) Interpretativa (tom/estética, não elemento ausente) |

---

## 2. QUEM SOMOS

| # | Divergência | Imagem de referência | Trecho exato | Classificação |
|---|---|---|---|---|
| QS1 | Breadcrumb "Home > Quem Somos" ausente | `quem-somos/image1.png` | Bloco "NAV — Navegação fixa — mesmo padrão da Home · Breadcrumb: Home › Quem Somos", com a linha `Home › Quem Somos` abaixo do menu | A) Objetiva (elemento de navegação ausente) |
| QS2 | Seção "Como Operamos" (4 pilares) ausente | `quem-somos/image4.png` | Bloco "SEÇÃO 5 — MODELO OPERACIONAL — Pergunta: Como opera? · 4 pilares com prova · Aprofundamento do bloco da Home", cards Varejo popular / Gestão padronizada / Compras em escala / Expansão contínua | A) Objetiva (seção ausente) |
| QS3 | Seção "Diferenciais Competitivos" (3 cards) ausente | `quem-somos/image4.png` | Bloco "SEÇÃO 6 — DIFERENCIAIS COMPETITIVOS — 3 diferenciais com argumentação", cards 01 Presença onde outros não chegam / 02 Modelo validado em diversidade regional / 03 Escala com gestão eficiente | A) Objetiva (seção ausente) |
| QS4 | Seção "Presença Nacional" (mapa + grid de estados) ausente | `quem-somos/image10.png` | Bloco "Ajuste 3 — Presença Nacional — título conceitual", com `[Mapa do Brasil — 14 estados em vermelho]` e grid de siglas (BA, CE, GO, MA / MG, MS, MT, PA / PE, PI, PR, RO / SP, TO) | A) Objetiva (seção ausente) |
| QS5 | CTA final "Relacionamentos Estratégicos" (4 cards) ausente — implementação usa CTA genérico de 1 botão | `quem-somos/image11.png` | Bloco "Ajuste 4 — CTA final — card Expansão reforçado", título "RELACIONAMENTOS ESTRATÉGICOS — Uma rede que cresce com seus parceiros. Qual é o seu próximo passo?", 4 cards Expansão (Público prioritário) / Imóveis / Fornecedores / Trabalhe Conosco | A) Objetiva (seção/cards ausentes) |
| QS6 | Overlay do hero | `quem-somos/image1.png` | Hero "SOBRE A SOL MAGAZINE" com gradiente decrescente esquerda→direita | B) Interpretativa |

---

## 3. PRESENÇA NACIONAL

| # | Divergência | Imagem de referência | Trecho exato | Classificação |
|---|---|---|---|---|
| PN1 | Overlay do hero uniforme em vez de localizado | `presenca-nacional/image15.png` | "Ajuste 1 — Hero — foto protagonista, gradiente localizado atrás do texto, área direita sem overlay"; "Princípio aplicado: O hero ocupa 100% da largura (...) protegendo legibilidade onde o texto está, revelado a foto vivível, e a barra de stats com fundo opaco a 62% de opacidade, mantendo a imagem visível ao fundo" | B) Interpretativa |
| PN2 | Cor da barra de credibilidade — **já confirmado aderente**, sem divergência | `presenca-nacional/image16.png` | "Rodapé definitivo" com barra `#1e0e0e` | — (sem divergência) |
| PN3 | Seções intermediárias (Mapa interativo, Tabela por Estado, Galeria Contextual, "Onde Continuamos Crescendo") não reconfirmadas | *(nenhuma — imagens 1–14 não foram revisadas nesta rodada)* | Não aplicável — pendência de verificação, não divergência confirmada | Não classificável (falta evidência de imagem) |

---

## 4. EXPANSÃO

| # | Divergência | Imagem de referência | Trecho exato | Classificação |
|---|---|---|---|---|
| EX1 | Overlay do hero | `expansao/image6.png` | "SEÇÃO 1 — HERO — Inalterado — Foto protagonista — 2 CTAs · 4 indicadores", gradiente no hero | B) Interpretativa |
| EX2 | Títulos/conteúdo das 7 etapas divergem | `expansao/image7.png` | Bloco "SEÇÃO 4 — COMO A EXPANSÃO ACONTECE", etapas 01 Identificação da oportunidade, 02 Análise de mercado, 03 Avaliação imobiliária, 04 Planejamento operacional, 05 Implantação, 06 Inauguração, 07 Operação consolidada | B) Interpretativa (a seção e a quantidade de etapas existem; diverge o texto/nome de cada etapa) |
| EX3 | "Modelo que Sustenta a Expansão" com 3 cards genéricos em vez de 4 pilares com indicador numérico | `expansao/image7.png` | Bloco "SEÇÃO 3 — MODELO QUE SUSTENTA A EXPANSÃO — 4 pilares com prova operacional", cards Varejo popular (+100 lojas) / Gestão padronizada (14 estados) / Compras em escala (+10 anos) / Expansão estruturada (Crescimento) | A) Objetiva (1 card ausente: são 4 no wireframe, 3 na implementação) — *componente numérico (indicador na base de cada card) também ausente, reforçando o caráter objetivo* |
| EX4 | "Critérios de Expansão" com nomes diferentes | `expansao/image8.png` | Bloco "SEÇÃO 5 — COMO AVALIAMOS NOVOS MERCADOS", cards "Localização estratégica", "Potencial de consumo", "Viabilidade operacional" | B) Interpretativa (quantidade de cards é a mesma — 3 —, diverge apenas o texto/nome) |
| EX5 | "O que é o Projeto de Expansão" sem os 3 cards (Investidores/Proprietários/Empreendedores) | `expansao/image8.png` | Bloco "SEÇÃO 6 — O QUE É O PROJETO DE EXPANSÃO", 3 cards: Investidores e parceiros / Proprietários de imóveis / Empreendedores e operadores, cada um com tag (Oportunidade de participação / Parceria imobiliária / Operação de unidades) | A) Objetiva (estrutura de 3 cards ausente — implementação usa bloco de texto livre) |
| EX6 | CTA final por perfil com card "Expansão"+"Contato" em vez de "Investidores e Parceiros" | `expansao/image9.png` | Bloco "SEÇÃO 8 — CTA POR PERFIL", cards: Investidores e Parceiros / Imóveis / Fornecedores / Trabalhe Conosco | A) Objetiva (card "Investidores e Parceiros" ausente; card "Contato" presente na implementação não existe no wireframe) |

---

## 5. IMÓVEIS

| # | Divergência | Imagem de referência | Trecho exato | Classificação |
|---|---|---|---|---|
| IM1 | Overlay do hero | `imoveis/image7.png` | Hero "IMÓVEIS", nota "Foto real · fachada do ponto comercial · overlay >40%" | B) Interpretativa |
| IM2 | "Por que Indicar seu Imóvel" com títulos de card diferentes | `imoveis/image8.png` | Bloco "POR QUE INDICAR SEU IMÓVEL", cards "Parceria de longo prazo", "Operação confiável e estruturada", "Expansão contínua e planejada" | B) Interpretativa (quantidade de cards igual — 3 —, diverge texto/título) |
| IM3 | Seção "Perfil que atende" (checklist 8 itens ✓/✗) ausente | `imoveis/image9.png` | Bloco "Perfil que atende", lista com ✓ Térreo com acesso direto à rua / ✓ Área mínima de [X] m² / ✓ Alto fluxo de pessoas / ✓ Boa visibilidade da fachada / Estacionamento ou facilidade de acesso (tag "novo — diferencial") / ✓ Localização em região comercial / ✗ Andares superiores sem acesso direto / ✗ Regiões com baixo fluxo | A) Objetiva (seção inteira ausente) |
| IM4 | Campo "Bairro/Região" ausente no formulário | `imoveis/image10.png` | Campo de input rotulado "Bairro / Região" na coluna "Dados do imóvel" | A) Objetiva (campo ausente) |
| IM5 | Campo "Tipo de imóvel" (select) ausente | `imoveis/image10.png` | Campo "Tipo de imóvel ▾" marcado em vermelho como obrigatório | A) Objetiva (campo ausente) |
| IM6 | Campo "Valor pretendido (R$)" ausente | `imoveis/image10.png` | Campo de input "Valor pretendido (R$)" | A) Objetiva (campo ausente) |
| IM7 | Campo "Situação atual" (select) ausente | `imoveis/image10.png` | Campo "Situação atual ▾" marcado em vermelho como obrigatório | A) Objetiva (campo ausente) |
| IM8 | Upload de fotos (fachada, interior, entorno) ausente | `imoveis/image10.png` | Campo de upload "↑ Fotos — fachada, interior e entorno" | A) Objetiva (campo ausente) |
| IM9 | Sidebar "O que analisamos em cada imóvel" / "Prazo de retorno" / "Dúvidas?" ausente | `imoveis/image10.png` | Bloco lateral direito: "O que analisamos em cada imóvel" (5 bullets) + "Prazo de retorno" + "Dúvidas? Canal de imóveis: imoveis@solmagazine.com.br" | A) Objetiva (bloco inteiro ausente) |

---

## 6. FORNECEDORES

| # | Divergência | Imagem de referência | Trecho exato | Classificação |
|---|---|---|---|---|
| FO1 | Overlay do hero | `fornecedores/image7.png` | Nota "Foto real · produtos / interior de loja · vermelho institucional — overlay >40%" | B) Interpretativa |
| FO2 | Categorias — **já confirmado aderente**, sem divergência | `fornecedores/image8.png` | Cards "Confecções e Moda Popular" / "Utilidades" / "Cama, Mesa e Banho" / "Acessórios" | — (sem divergência) |
| FO3 | Falta o 4º critério "Regularidade cadastral e documental" | `fornecedores/image8.png` | Bloco "Ad.4 — O que analisamos — critério documental adicionado", card 04 "Regularidade cadastral e documental" (tag "novo") — *fornecedores homologados precisam estar com situação fiscal e cadastral regular* | A) Objetiva (card/critério ausente — 4 no wireframe, 3 na implementação) |
| FO4 | Campo "Cargo" ausente no formulário | `fornecedores/image9.png` | Campo de input "Cargo" na coluna "Dados da empresa" | A) Objetiva (campo ausente) |
| FO5 | Campos "Cidade sede" / "Estado sede" ausentes | `fornecedores/image9.png` | Campos "Cidade sede" e "Estado sede ▾" | A) Objetiva (campos ausentes) |
| FO6 | Campo "Site ou portfólio (opcional)" ausente | `fornecedores/image9.png` | Campo de input "Site ou portfólio de produtos (opcional)" | A) Objetiva (campo ausente) |
| FO7 | Campo "Capacidade mensal aproximada" ausente | `fornecedores/image9.png` | Campo de input "Capacidade mensal aproximada" | A) Objetiva (campo ausente) |
| FO8 | Campo "Estado(s) de atuação / cobertura logística" ausente | `fornecedores/image9.png` | Campo "Estado(s) de atuação / cobertura logística ▾" (tag "novo") | A) Objetiva (campo ausente) |
| FO9 | Upload de catálogo/apresentação ausente | `fornecedores/image9.png` | Campo de upload "↑ Catálogo, apresentação ou tabela comercial (PDF, opcional)" (tag "renomeado") | A) Objetiva (campo ausente) |
| FO10 | Sidebar "Categorias com demanda ativa" / "O que analisamos" / "Prazo de retorno" / "Canal de fornecedores" ausente | `fornecedores/image9.png` | Bloco lateral direito completo | A) Objetiva (bloco inteiro ausente) |

---

## 7. TRABALHE CONOSCO

| # | Divergência | Imagem de referência | Trecho exato | Classificação |
|---|---|---|---|---|
| TC1 | Overlay do hero | `trabalhe-conosco/image13.png` | Hero "Faça parte de uma rede em crescimento real" com gradiente | B) Interpretativa |
| TC2 | Indicador "14 estados brasileiros" — **já confirmado aderente**, sem divergência | `trabalhe-conosco/image13.png` | "Aj.1 — Hero — '14 estados brasileiros' (padronizado)" | — (sem divergência) |
| TC3 | História nº2 genérica — **já confirmado aderente**, sem divergência | `trabalhe-conosco/image13.png` | "Aj.2 — História nº 2 — placeholder genérico e flexível", texto "Depois — genérico e flexível ✓" | — (sem divergência) |
| TC4 | Campo "Experiência na área" deveria ser select, implementado como textarea | `trabalhe-conosco/image14.png` | Bloco "Aj.3 — Formulário — campos de localização revisados", coluna "Depois ✓": "Experiência na área ▾" (formato dropdown, com seta indicando select) | A) Objetiva (tipo de campo incorreto — select esperado, textarea implementado; não é apenas redação, é um componente de UI diferente) |
| TC5 | Rótulo "Experiência" abreviado em vez de "Experiência na área" | `trabalhe-conosco/image14.png` | Mesmo campo "Experiência na área ▾" citado acima | B) Interpretativa (diferença apenas de rótulo/texto) |
| TC6 | Ordem dos campos do formulário possivelmente diferente | `trabalhe-conosco/image14.png` | Coluna "Depois ✓": ordem Disponibilidade para início → Experiência na área → Cidade atual → Disponibilidade para mudança | B) Interpretativa (não verificado com certeza; depende de leitura de ordem visual, não é um campo ausente) |

---

## 8. CONTATO

| # | Divergência | Imagem de referência | Trecho exato | Classificação |
|---|---|---|---|---|
| CO1 | Overlay do hero | `contato/image5.png` | "Hero definitivo — Alternativa B", bloco escuro com gradiente | B) Interpretativa |
| CO2 | Hero Alternativa B — **já confirmado aderente**, sem divergência | `contato/image5.png` | "Fale com a Sol Magazine. / Direcionamos sua mensagem para a área responsável." | — (sem divergência) |
| CO3 | 5 canais por assunto — **já confirmado aderente**, sem divergência | `contato/image6.png` | Cards Expansão e investimento / Imóveis / Fornecedores / RH e Carreiras / Contato geral, com e-mails | — (sem divergência) |
| CO4 | Campo "Empresa/Organização (opcional)" ausente no formulário | `contato/image7.png` | Bloco "Seus dados", campo de input "Empresa / Organização (opcional)" | A) Objetiva (campo ausente) |
| CO5 | Campo "Sede" ausente na sidebar | `contato/image7.png` | Bloco "Informações corporativas", linha "Sede — [Cidade / Estado — placeholder]" | A) Objetiva (campo ausente) |
| CO6 | Redes sociais (Instagram/LinkedIn) — **já confirmado aderente**, sem divergência | `contato/image8.png` | Rodapé "Contato — Fale Conosco — Instagram — LinkedIn" | — (sem divergência) |

---

## Tabela Final — Divergências Objetivas × Interpretativas por Página

| Página | Divergências Objetivas (A) | Divergências Interpretativas (B) |
|---|---|---|
| Home | 7 (H2, H3, H4, H5, H6, H7, H8) | 2 (H1, H9) |
| Quem Somos | 5 (QS1, QS2, QS3, QS4, QS5) | 1 (QS6) |
| Presença Nacional | 0 | 1 (PN1) |
| Expansão | 3 (EX3, EX5, EX6) | 2 (EX2, EX4) |
| Imóveis | 7 (IM3, IM4, IM5, IM6, IM7, IM8, IM9) | 2 (IM1, IM2) |
| Fornecedores | 8 (FO3, FO4, FO5, FO6, FO7, FO8, FO9, FO10) | 1 (FO1) |
| Trabalhe Conosco | 1 (TC4) | 3 (TC1, TC5, TC6) |
| Contato | 2 (CO4, CO5) | 1 (CO1) |
| **Transversal (overlay do hero)** | 0 | 1 |
| **Total** | **33** | **13** |

---

## Leitura para decisão de correção

- **Divergências objetivas (33 no total)** são as que exigem desenvolvimento concreto e inequívoco: criação de seções/cards/campos que hoje **não existem no código**. Não há ambiguidade de interpretação — é uma questão de existir ou não existir.
- **Divergências interpretativas (13 no total)** dependem de uma decisão de produto/design antes de qualquer ajuste de código: por exemplo, o tratamento do overlay do hero (gradiente localizado vs. cor sólida) é uma escolha estética que pode ser mantida como está, revertida ao padrão do wireframe, ou ajustada de outra forma — todas são tecnicamente viáveis, a diferença é de critério, não de ausência de funcionalidade.
- Os itens marcados como "**já confirmado aderente, sem divergência**" (PN2, FO2, TC2, TC3, CO2, CO3, CO6) foram re-confirmados nesta validação e **não exigem nenhuma ação**.
- O item PN3 (seções intermediárias de Presença Nacional) não pôde ser classificado como divergência por falta de imagem de evidência revisada nesta rodada — é uma pendência de verificação, não uma divergência confirmada.

Nenhuma alteração de código foi realizada nesta etapa.
