# Auditoria de Aderência aos Wireframes Homologados

> Etapa 2 da auditoria. Objetivo: comparar o protótipo HTML implementado (8 páginas + `styles.css`) contra as versões homologadas identificadas na Etapa 1 (`VERSOES_HOMOLOGADAS_IDENTIFICADAS.md`), o `Dossiê Oficial Sol Magazine 2026.pdf`, e as confirmações do usuário sobre Home (Refinada v2), Expansão (v2) e Contato (Hero Alternativa B). **Nenhuma correção de código foi feita nesta etapa** — apenas levantamento e classificação de divergências.

## Critério de gravidade

- **CRÍTICA**: contradiz uma decisão explicitamente homologada (texto, estrutura, dado obrigatório) ou compromete a navegação/arquitetura de informação definida no Dossiê.
- **MÉDIA**: diverge de conteúdo/estrutura homologada mas não compromete a navegação ou a regra de negócio central da página.
- **PEQUENA**: diferença pontual de redação, ordem ou detalhe visual sem impacto funcional.

---

## Divergências transversais (afetam todas as páginas)

### 1. Menu principal sem agrupamento "Oportunidades"
- **Página**: Todas (header global).
- **Seção**: `site-header` / `.nav-links`.
- **Situação atual**: menu plano com 8 itens (Home, Quem Somos, Presença Nacional, Expansão, Imóveis, Fornecedores, Trabalhe Conosco, Contato) — confirmado em `styles.css` (`.nav-links` é lista simples, sem submenu/dropdown) e em todos os HTMLs.
- **Situação homologada**: Dossiê Oficial, seção 5 — menu deve ser Home / Quem Somos / Presença Nacional / **Oportunidades** (submenu: Expansão, Imóveis, Fornecedores, Trabalhe Conosco) / Contato.
- **Gravidade**: CRÍTICA.
- **Impacto**: arquitetura de informação e hierarquia de navegação divergem do que foi homologado; usuário não percebe o agrupamento de "oportunidades de negócio" pretendido.
- **Correção necessária**: implementar item de menu "Oportunidades" com dropdown contendo Expansão, Imóveis, Fornecedores e Trabalhe Conosco, reduzindo o menu principal a 5 itens visíveis + Contato.

### 2. Overlay do hero fora da faixa homologada
- **Página**: Todas com `.hero` (Home, Quem Somos, Presença Nacional, Expansão, Imóveis, Fornecedores, Trabalhe Conosco) e variante `.hero-neutro` (Contato).
- **Seção**: `styles.css`, regra `.hero::before`.
- **Situação atual**: `linear-gradient(90deg, rgba(28,18,18,.84) 0%, rgba(28,18,18,.55) 38%, rgba(28,18,18,0) 60%)` — gradiente direcional que vai de 84% de opacidade a 0%, confirmado visualmente no screenshot `index_desktop.png` (lado esquerdo escuro, lado direito sem overlay).
- **Situação homologada**: Dossiê Oficial, observação geral — overlay deve ser uma faixa **plana** entre 38% e 42% de opacidade, nunca superior a 60%.
- **Gravidade**: CRÍTICA.
- **Impacto**: legibilidade do texto do hero e identidade visual divergem do padrão homologado; o gradiente atual chega a 84%, mais que o dobro do teto de 60% definido.
- **Correção necessária**: substituir o gradiente direcional por um overlay de cor sólida (ou gradiente muito sutil) fixado entre 38% e 42% de opacidade em todas as heroes.

### 3. Barra de credibilidade sem cor de fundo própria
- **Página**: Todas (footer global, `.footer-credibility`).
- **Seção**: `styles.css`, `.site-footer` / `.footer-credibility`.
- **Situação atual**: `.site-footer` usa `--rodape: #271414` para todo o rodapé; `.footer-credibility .stats-bar` usa `background: transparent`, herdando o mesmo `#271414` do rodapé institucional — confirmado no CSS (linhas 505–513).
- **Situação homologada**: Dossiê Oficial — cor de fundo homologada `#1e0e0e` para a barra de credibilidade (indicadores +100/14/+10), distinta do `#271414` do restante do rodapé.
- **Gravidade**: PEQUENA.
- **Impacto**: diferença visual sutil de tonalidade; não compromete funcionalidade nem leitura, mas é uma especificação explícita do Dossiê não atendida.
- **Correção necessária**: aplicar `background: #1e0e0e` em `.footer-credibility`, mantendo `#271414` apenas em `.footer-main`/`.footer-bottom`.

---

## HOME (`index.html`)

> Versão homologada de referência: **Home Refinada v2** (confirmado pelo usuário).

### H1. Bloco de cards sem o rótulo "Relacionamentos Estratégicos"
- **Seção**: bloco de 3 cards (Imóveis / Fornecedores / Trabalhe Conosco), entre "Projeto de Expansão" e o CTA final.
- **Situação atual**: bloco de 3 cards sem `section-eyebrow`/título de seção identificando o agrupamento.
- **Situação homologada**: Dossiê Oficial, seção 8 — esta área é nomeada "Relacionamentos Estratégicos".
- **Gravidade**: MÉDIA.
- **Impacto**: perde-se o conceito de "ecossistema de parceiros" que o nome pretende comunicar; visualmente os cards parecem 3 atalhos isolados em vez de uma seção com identidade própria.
- **Correção necessária**: adicionar `section-eyebrow` "Relacionamentos Estratégicos" e `h2` de apoio antes do grid de 3 cards.

---

## QUEM SOMOS (`quem-somos.html`)

> Versão homologada de referência: base (imagens 1–8) + ajustes (imagens 9–11) sobre as seções correspondentes.

### QS1. Estrutura geral aderente
- A estrutura implementada (Hero, História, Modelo Operacional, Pilares, Linha do Tempo, CTA Expansão, Rodapé) confere com a seção 9 do Dossiê.
- **Gravidade**: sem divergência estrutural relevante identificada nesta etapa para esta página, alem das transversais (menu/overlay/cor).

---

## PRESENÇA NACIONAL (`presenca-nacional.html`)

> Versão homologada de referência: "segundo ajuste" (imagens 15–16), congelada.

### PN1. Estrutura geral aderente
- Hero com título/subtítulo/indicadores, Mapa do Brasil, Presença por Região, Tabela por Estado, Galeria Contextual, "Onde Continuamos Crescendo", CTA Institucional e Rodapé — todos presentes e na ordem esperada conforme seção 10 do Dossiê.
- **Gravidade**: sem divergência estrutural relevante identificada nesta etapa, além das transversais.

---

## EXPANSÃO (`expansao.html`)

> Versão homologada de referência: **Expansão v2** ("pronta para homologação", confirmado pelo usuário como estágio final).

### EX1. Conteúdo da seção "Como a Expansão Acontece" não corresponde ao processo homologado
- **Seção**: bloco de etapas/processo de expansão.
- **Situação atual**: a implementação apresenta um fluxo de etapas que não reflete o conteúdo de 7 passos descrito na versão v2 do wireframe (conteúdo de processo divergente do texto detalhado nas imagens de ajuste).
- **Situação homologada**: Dossiê Oficial, seção 13, e wireframe v2 — "Como a Expansão Acontece" deve detalhar o processo completo conforme descrito nas imagens 6–12 do `.docx`.
- **Gravidade**: MÉDIA.
- **Impacto**: usuário interessado em abrir uma unidade recebe informação de processo incompleta/diferente da homologada.
- **Correção necessária**: revisar o conteúdo textual da seção de processo para refletir os passos detalhados na versão v2.

### EX2. Página mantém caráter institucional, sem duplicar a Landing de Expansão
- A implementação não duplica conteúdo de landing page e direciona corretamente via CTA — aderente à diretriz do Dossiê de que esta página deve "apenas direcionar".
- **Gravidade**: sem divergência.

---

## IMÓVEIS (`imoveis.html`)

> Versão homologada de referência: ajuste único (imagens 7–10), com "Diferenciais Homologados" do Dossiê.

### IM1. Ausência do campo "Link Google Maps (opcional)"
- **Seção**: formulário de cadastro de imóvel.
- **Situação atual**: formulário não contém campo para link do Google Maps.
- **Situação homologada**: Dossiê Oficial, seção "Diferenciais Homologados" — campo "Link Google Maps (opcional)" deve constar no formulário.
- **Gravidade**: CRÍTICA (item explicitamente listado como "Homologado" no Dossiê).
- **Impacto**: perda de informação de localização estruturada para análise de imóveis recebidos.
- **Correção necessária**: adicionar campo de texto opcional "Link Google Maps" ao formulário.

### IM2. Estacionamento tratado como obrigatório/ausente em vez de diferencial opcional
- **Seção**: formulário/critérios de imóvel.
- **Situação atual**: não há tratamento específico do campo "estacionamento" como diferencial não obrigatório (ausente ou implícito).
- **Situação homologada**: Dossiê — "estacionamento é diferencial, não obrigatório", deve constar como opção/checkbox claramente não obrigatória.
- **Gravidade**: MÉDIA.
- **Impacto**: critério de triagem de imóveis não fica explícito para quem preenche o formulário.
- **Correção necessária**: incluir campo "Possui estacionamento (diferencial, não obrigatório)" no formulário.

---

## FORNECEDORES (`fornecedores.html`)

> Versão homologada de referência: ajuste único (imagens 7–9).

### FO1. Estrutura geral aderente
- Hero, "Por que fornecer", Categorias (Confecções e Moda Popular / Utilidades / Cama, Mesa e Banho / Acessórios), Critérios (capacidade de abastecimento, custo-benefício, logística, regularidade cadastral e documental), Processo, Formulário, CTA e Rodapé — todos presentes conforme seção 12 do Dossiê.
- **Gravidade**: sem divergência estrutural relevante identificada nesta etapa, além das transversais.

---

## TRABALHE CONOSCO (`trabalhe-conosco.html`)

> Versão homologada de referência: "Versão Final Homologada" — simplificada (~35% menor que o wireframe inicial) — e "Ajustes Finais Homologados" (4 itens pontuais).

### TC1. Ausência do indicador "14 estados brasileiros"
- **Seção**: hero ou bloco de indicadores da página.
- **Situação atual**: a página não exibe o indicador "14 estados brasileiros" em nenhum ponto do conteúdo (apenas presente no rodapé global como "14 Estados Atendidos", não como destaque proprietário da página).
- **Situação homologada**: Dossiê Oficial, seção 14, "Ajustes Finais Homologados" — indicador "14 estados brasileiros" deve estar presente na página.
- **Gravidade**: MÉDIA.
- **Impacto**: argumento de escala/alcance nacional, relevante para atrair candidatos, não é reforçado no corpo da página.
- **Correção necessária**: inserir o indicador "14 estados brasileiros" em destaque (hero ou seção "Como é Trabalhar Aqui").

### TC2. Histórias de Crescimento não estão em "versão genérica e flexível"
- **Seção**: "Histórias de Crescimento" (3 cards de depoimento).
- **Situação atual**: os 3 cards usam o mesmo texto-placeholder genérico ("Colaborador(a)" / "Depoimento real a ser inserido na versão final"), sem diferenciação ou estrutura de história nº2 conforme especificado.
- **Situação homologada**: Dossiê — "História nº2 em versão genérica e flexível" é um dos 4 ajustes finais homologados, sugerindo que ao menos uma das histórias deveria ter um texto-modelo genérico (não apenas placeholder neutro) que sirva de molde reaproveitável.
- **Gravidade**: PEQUENA.
- **Impacto**: baixo nesta fase de protótipo, pois todo o bloco já está marcado como placeholder; mas o ajuste homologado pede um texto-modelo específico, não apenas "placeholder".
- **Correção necessária**: redigir um texto-modelo genérico e flexível para a "História nº2", mantendo as demais como placeholder.

### TC3. Formulário de candidatura sem os 4 campos homologados
- **Seção**: `#formulario`, formulário de candidatura.
- **Situação atual**: campos presentes são Nome completo, Telefone, E-mail, Cidade/Estado, Área de interesse, Currículo, Mensagem. Não há campos "Disponibilidade para Mudança", "Experiência" e "Disponibilidade para Início" (apenas "Cidade Atual" está parcialmente coberto por "Cidade/Estado").
- **Situação homologada**: Dossiê Oficial, seção 14, "Ajustes Finais Homologados" — formulário deve conter explicitamente os campos "Cidade Atual", "Disponibilidade para Mudança", "Experiência" e "Disponibilidade para Início".
- **Gravidade**: CRÍTICA (4 campos explicitamente homologados, 3 deles totalmente ausentes).
- **Impacto**: triagem de candidatos perde informações estruturadas essenciais (mobilidade, senioridade, prazo de início), que precisariam ser coletadas manualmente depois.
- **Correção necessária**: renomear "Cidade/Estado" para "Cidade Atual" e adicionar os campos "Disponibilidade para Mudança" (select sim/não), "Experiência" (texto/textarea) e "Disponibilidade para Início" (texto/select).

### TC4. Página não reflete a redução de ~35% mencionada na versão final homologada
- **Seção**: página como um todo.
- **Situação atual**: a página tem 8 seções (Hero, Como é Trabalhar Aqui, Áreas de Atuação, Histórias de Crescimento, Processo Seletivo, Formulário, CTA Final) — não é possível confirmar objetivamente a redução de 35% sem contagem comparativa de blocos do wireframe inicial completo, mas a estrutura aparenta manter todas as seções do wireframe sem simplificação visível.
- **Situação homologada**: Dossiê — versão final é "simplificada, com redução de aproximadamente 35% em relação ao wireframe inicial".
- **Gravidade**: PEQUENA (achado qualitativo, não quantificável com precisão nesta etapa).
- **Impacto**: indica que a página pode estar mais extensa do que a versão homologada pretendia.
- **Correção necessária**: revisão de conteúdo na fase de correção, comparando blocos do wireframe inicial (imagens 1–6) com a versão final, para identificar quais seções deveriam ser reduzidas/condensadas.

---

## CONTATO (`contato.html`)

> Versão homologada de referência: "Ajustes" (imagens 5–10 + PNG solto nº2), com Hero Alternativa B confirmada pelo usuário ("Fale com a Sol Magazine." / "Direcionamos sua mensagem para a área responsável.").

### CO1. Hero não usa o subtítulo da Alternativa B homologada
- **Seção**: `.hero.hero-neutro`.
- **Situação atual**: título "Fale com a Sol Magazine" (sem ponto final) e subtítulo "Escolha o canal certo para o seu assunto ou utilize o formulário único abaixo."
- **Situação homologada**: Hero Alternativa B confirmada pelo usuário — título "Fale com a Sol Magazine." (com ponto final) e subtítulo "Direcionamos sua mensagem para a área responsável."
- **Gravidade**: CRÍTICA (decisão explícita do usuário sobre qual alternativa de hero é a oficial, e o texto atual não corresponde a nenhuma das duas variantes esperadas com exatidão).
- **Impacto**: a página exibe um texto de hero que não é a versão final homologada, alterando o tom da comunicação (orientação para o usuário escolher canal vs. promessa de direcionamento automático pela equipe).
- **Correção necessária**: substituir h1 por "Fale com a Sol Magazine." e o parágrafo do hero por "Direcionamos sua mensagem para a área responsável."

### CO2. Sidebar institucional sem o campo "Razão social"
- **Seção**: `aside` / `.sidebar-card` "Sol Magazine".
- **Situação atual**: sidebar lista Endereço da sede, Horário de atendimento e CNPJ (todos placeholder), mas não inclui um campo de Razão Social.
- **Situação homologada**: wireframe homologado especifica campo "Razão social: Sol Magazine Participações Ltda." na sidebar corporativa.
- **Gravidade**: MÉDIA.
- **Impacto**: informação societária formal, relevante para parceiros/investidores que acessam a página de contato, não está disponível.
- **Correção necessária**: adicionar linha "Razão social: Sol Magazine Participações Ltda." na `.sidebar-card` "Sol Magazine".

### CO3. Redes sociais com ícone extra não previsto no wireframe
- **Seção**: `.social-row`.
- **Situação atual**: 3 ícones — Instagram (IG), LinkedIn (IN), Facebook (FB).
- **Situação homologada**: wireframe homologado especifica apenas 2 redes sociais — Instagram e LinkedIn.
- **Gravidade**: PEQUENA.
- **Impacto**: inclusão de um canal (Facebook) não confirmado/homologado, podendo gerar expectativa de canal de atendimento que talvez nem seja mantido pela empresa.
- **Correção necessária**: remover o ícone/link do Facebook, mantendo apenas Instagram e LinkedIn.

### CO4. Estrutura de canais e formulário aderente
- 5 canais (Expansão e Investimento, Imóveis, Fornecedores, RH e Carreiras, Contato Geral), formulário único e estrutura geral conferem com a seção 15 do Dossiê.
- **Gravidade**: sem divergência nesse ponto.

---

## Observação metodológica

Esta auditoria foi feita por comparação textual/estrutural entre o HTML/CSS implementado, o conteúdo dos wireframes homologados (extraído na Etapa 1) e o Dossiê Oficial, complementada por inspeção visual de screenshots desktop para confirmar os achados de CSS (overlay, menu, cores). Nenhuma alteração de código foi realizada. As correções listadas servem de insumo para a próxima fase, mediante autorização explícita do usuário.
