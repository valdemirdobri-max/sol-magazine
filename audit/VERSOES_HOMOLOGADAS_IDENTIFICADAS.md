# Versões Homologadas Identificadas

> Etapa 1 da auditoria de aderência. Objetivo: identificar, dentro de cada arquivo de wireframe enviado (`Wiriframes homologados.zip`) e do `Dossiê Oficial Sol Magazine 2026.pdf`, qual é a **versão final homologada** de cada página — distinguindo-a de versões intermediárias, rascunhos e ajustes anteriores. Nenhuma correção de código foi feita nesta etapa.

## Fontes analisadas

- `Wiriframes homologados.zip` → 8 pastas (`01-home` a `08-contato`), cada uma com 1 arquivo `.docx` contendo as telas de wireframe como imagens embutidas, em ordem sequencial. A pasta `08-contato` também contém 2 arquivos `.png` soltos, fora do `.docx`.
- `Dossiê Oficial Sol Magazine 2026.pdf` → documento mestre, com seção dedicada a cada página (objetivo, hero, estrutura) e, em 2 casos (Trabalhe Conosco e Contato), uma seção explícita de "Versão Final Homologada" / "Ajustes Finais Homologados".

## Critério de identificação

Dentro de cada `.docx`, as imagens aparecem em ordem cronológica. Quando existe um título textual entre blocos de imagens (ex.: "AJUSTES DA PÁGINA IMOVEIS", "Presença Nacional – segundo ajuste"), tudo o que vem **depois** desse título é revisão sobre o que vem antes. Quando o Dossiê Oficial confirma explicitamente uma versão como final ("Versão Final Homologada", "Ajustes Finais Homologados", "Diferenciais Homologados"), essa confirmação têm prioridade sobre a ordem do arquivo.

---

## HOME

- **Versão identificada**: única versão (sem marcador de ajuste no arquivo).
- **Arquivo utilizado**: `01-home/Wiriframes Home.docx` — 6 imagens, sequência única, sem texto de revisão entre elas.
- **Situação**: Homologada (não há indicação de versão intermediária neste arquivo).
- **Justificativa**: o documento não contém nenhum título de "ajuste" ou "versão" — é um bloco fechado de 6 telas. O Dossiê Oficial (seção 8) confirma a estrutura: Hero, Quem Somos, Presença Nacional, Projeto de Expansão, Relacionamentos Estratégicos, Contato, Rodapé.
- **Atenção para a Etapa 2**: o Dossiê nomeia a seção de cards como "**Relacionamentos Estratégicos**" — a implementação atual rotula essa mesma área como bloco de 3 cards (Imóveis/Fornecedores/Trabalhe Conosco), sem esse nome. A ser tratado como divergência na auditoria de aderência.

## QUEM SOMOS

- **Versão identificada**: versão com ajustes aplicados (imagens 9–11 sobre a base 1–8).
- **Arquivo utilizado**: `02-quem-somos/Wiriframes Quem somos.docx` — imagens 1–8 (versão inicial completa), depois o texto "Telas geradas após ajustes em algumas seções.", depois imagens 9–11 (telas revisadas).
- **Situação**: Homologada (ajustes parciais).
- **Justificativa**: o texto interno do documento indica explicitamente que as imagens finais (9–11) substituem **apenas as seções que foram ajustadas** — as demais seções permanecem como nas imagens 1–8. A versão homologada final é, portanto, um composto: base 1–8 + substituições 9–11 nas seções correspondentes. O Dossiê Oficial (seção 9) confirma a estrutura: Hero, História, Modelo Operacional, Pilares, Linha do Tempo, CTA Expansão, Rodapé.

## PRESENÇA NACIONAL

- **Versão identificada**: "Presença Nacional – segundo ajuste" (imagens 15–16).
- **Arquivo utilizado**: `03-presenca-nacional/Wiriframe Presença Nacional.docx` — imagens 1–7 (versão inicial), título "Presença Nacional – primeiro ajuste" + imagens 8–14, título "Presença Nacional – segundo ajuste" + imagens 15–16.
- **Situação**: Homologada e Congelada (última revisão registrada no arquivo).
- **Justificativa**: há duas rodadas de ajuste explícitas e nomeadas em sequência; a segunda rodada (imagens 15–16) é necessariamente a mais recente. O Dossiê Oficial (seção 10) confirma hero oficial com título/subtítulo/indicadores e a estrutura: Mapa do Brasil, Presença por Região, Tabela por Estado, Galeria Contextual, Onde Continuamos Crescendo, CTA Institucional, Rodapé.

## EXPANSÃO

- **Versão identificada**: "AJUSTES PAGINA EXPANSÃO" (imagens 6–12).
- **Arquivo utilizado**: `06-expansao/Wiriframa Expansão.docx` — imagens 1–5 (versão inicial), título "AJUSTES PAGINA EXPANSÃO" + imagens 6–12.
- **Situação**: Homologada (ajuste único, sem rodada posterior registrada).
- **Justificativa**: única rodada de ajuste no arquivo, vindo depois da versão inicial. O Dossiê Oficial (seção 13) reforça que esta é uma página institucional, **não landing page**, com estrutura: Como Crescemos, Modelo que Sustenta a Expansão, Como a Expansão Acontece, Critérios de Expansão, O que é o Projeto de Expansão, CTA para Landing, CTA por Perfil, Rodapé — e confirma que a Landing de Expansão é projeto separado, e que esta página deve **apenas direcionar**, sem duplicar conteúdo.

## IMÓVEIS

- **Versão identificada**: "AJUSTES DA PÁGINA IMOVEIS" (imagens 7–10).
- **Arquivo utilizado**: `04-imoveis/Wiriframe Imoveis.docx` — imagens 1–6 (versão inicial), título "AJUSTES DA PÁGINA IMOVEIS" + imagens 7–10.
- **Situação**: Homologada e Congelada — o Dossiê Oficial reforça com uma seção própria de "**Diferenciais Homologados**" (seção 11), que detalha: campo "Link Google Maps (opcional)" e o critério "estacionamento é diferencial, não obrigatório" — confirmando que a versão final inclui esses 2 itens.
- **Justificativa**: única rodada de ajuste no arquivo + confirmação textual explícita no Dossiê com o termo "Homologados".

## FORNECEDORES

- **Versão identificada**: "AJUSTE PAGINA FORNECEDORES" (imagens 7–9).
- **Arquivo utilizado**: `05-fornecedores/Wiriframe Fornecedores.docx` — imagens 1–6 (versão inicial), título "AJUSTE PAGINA FORNECEDORES" + imagens 7–9.
- **Situação**: Homologada (ajuste único, sem rodada posterior registrada).
- **Justificativa**: única rodada de ajuste no arquivo. O Dossiê Oficial (seção 12) confirma hero, categorias (Confecções e Moda Popular / Utilidades / Cama, Mesa e Banho / Acessórios), critérios (capacidade de abastecimento, custo-benefício, logística, regularidade cadastral e documental) e estrutura: Hero, Por que fornecer, Categorias, Critérios, Processo, Formulário, CTA, Rodapé.

## TRABALHE CONOSCO

- **Versão identificada**: "SEGUNDO AJUSTE PAGINA TRABALHE CONOSCO" (imagens 13–14).
- **Arquivo utilizado**: `07-trabalhe-conosco/Wiriframe trabalhe conosco.docx` — imagens 1–6 (versão inicial), título "PRIMEIROS AJUSTES PAGINA TRABALHE CONOSCO" + imagens 7–12, título "SEGUNDO AJUSTE PAGINA TRABALHE CONOSCO" + imagens 13–14.
- **Situação**: **Oficialmente Homologada** — esta é a página com a confirmação mais explícita de todo o pacote. O Dossiê Oficial (seção 14) tem uma subseção literalmente chamada "**Versão Final Homologada**", afirmando: versão simplificada, com redução de aproximadamente 35% em relação ao wireframe inicial. Em seguida há ainda uma subseção "**Ajustes Finais Homologados**" detalhando 4 itens pontuais: indicador "14 estados brasileiros", História nº2 em "versão genérica e flexível", e no formulário os campos "Cidade Atual", "Disponibilidade para Mudança", "Experiência" e "Disponibilidade para Início".
- **Justificativa**: dupla confirmação — ordem das imagens no `.docx` (segundo ajuste é o mais recente) **e** texto explícito do Dossiê rotulando esta como a versão final, com detalhamento dos últimos ajustes pontuais que devem estar presentes mesmo que não apareçam claramente nas imagens 13–14 isoladas.

## CONTATO

- **Versão identificada**: "AJUSTES PAGINA CONTATO" (imagens 5–10 do `.docx`) + arquivo solto `2 - Contato - ajustes.png`.
- **Arquivos utilizados**:
  - `08-contato/Wiriframe contato.docx` — imagens 1–4 (versão inicial), título "AJUSTES PAGINA CONTATO" + imagens 5–10.
  - `08-contato/1 - Contato_V2.png` — arquivo solto, fora do `.docx`, nomeado "V2".
  - `08-contato/2 - Contato - ajustes.png` — arquivo solto, nomeado "ajustes", numerado **depois** do V2.
- **Situação**: Homologada e Congelada — a numeração externa (`1 - ... V2` → `2 - ... ajustes`) e o título interno do `.docx` ("AJUSTES PAGINA CONTATO", segundo bloco de imagens) apontam na mesma direção: a versão "ajustes" é posterior à V2 e é a mais recente disponível.
- **Justificativa**: dois sinais independentes de versionamento (numeração de arquivo e título interno) concordam sobre qual é a versão mais recente. O Dossiê Oficial (seção 15) confirma hero oficial com título "Fale com a Sol Magazine." e subtítulo, 5 canais (Expansão e Investimento, Imóveis, Fornecedores, RH e Carreiras, Contato Geral), e estrutura: Cards de Canal, Formulário, Sidebar Corporativa, Redes Sociais, Rodapé.

---

## Resumo

| Página | Versão homologada identificada | Situação |
|---|---|---|
| Home | Única versão (6 imagens) | Homologada |
| Quem Somos | Base + ajustes parciais (imagens 9–11 sobre 1–8) | Homologada |
| Presença Nacional | Segundo ajuste (imagens 15–16) | Homologada e Congelada |
| Expansão | Ajuste único (imagens 6–12) | Homologada |
| Imóveis | Ajuste único (imagens 7–10) + Diferenciais Homologados do Dossiê | Homologada e Congelada |
| Fornecedores | Ajuste único (imagens 7–9) | Homologada |
| Trabalhe Conosco | Segundo ajuste (imagens 13–14) — rotulada "Versão Final Homologada" no Dossiê | Oficialmente Homologada |
| Contato | "Ajustes" (imagens 5–10 + PNG solto nº 2) | Homologada e Congelada |

## Observação sobre o Dossiê Oficial

O `Dossiê Oficial Sol Magazine 2026.pdf` estabelece, na sua própria seção 1, a hierarquia de prevalência: **Wireframes homologados > Dossiê Oficial > código implementado**. Ele também define 3 pontos que não estavam claros nos materiais anteriores e que serão usados como referência na Etapa 2 (auditoria de aderência):

1. **Menu Principal com agrupamento "Oportunidades"** (seção 5): o Dossiê descreve o menu oficial como Home / Quem Somos / Presença Nacional / **Oportunidades** (submenu: Expansão, Imóveis, Fornecedores, Trabalhe Conosco) / Contato — ou seja, **existe sim um agrupamento por dropdown previsto**, item que o protótipo HTML atual não implementa (menu plano de 8 itens).
2. **Overlay do hero**: faixa homologada de **38% a 42%**, nunca superior a 60% (o protótipo atual implementa um gradiente de 84%→0%, não uma faixa plana nesse intervalo).
3. **Barra de credibilidade**: cor de fundo homologada **`#1e0e0e`** para a barra de credibilidade, distinta do fundo escuro institucional geral **`#271414`** (o protótipo atual usa `#271414` para ambos, sem diferenciar a barra de indicadores do restante do rodapé).

Esses 3 pontos, junto com os "Diferenciais Homologados" (Imóveis) e "Ajustes Finais Homologados" (Trabalhe Conosco, Contato), serão a base de comparação central na Etapa 2.

---

**Aguardando validação desta identificação antes de prosseguir para a Etapa 2 (Auditoria de Aderência aos Wireframes).**
