# Inventário das Páginas

> Levantamento página a página do protótipo HTML implementado, conforme a arquitetura homologada no briefing. "Seções removidas" refere-se a itens previstos no briefing e ausentes na implementação; "seções adicionadas" refere-se a itens implementados sem previsão explícita no briefing.

---

## HOME

**Seções existentes** (na ordem em que aparecem):
1. Hero principal (eyebrow "Varejo Popular Nacional", CTAs duplos)
2. Quem Somos (resumo, com galeria de 2 imagens)
3. Presença Nacional (resumo, com barra de indicadores)
4. Projeto de Expansão (bloco texto + imagem)
5. Bloco de 3 cards (Imóveis / Fornecedores / Trabalhe Conosco)
6. CTA final (faixa escura)
7. Rodapé

**Seções removidas**: nenhuma — a estrutura segue exatamente a lista do briefing (Hero, Quem Somos resumo, Presença Nacional resumo, Expansão, Imóveis, Fornecedores, Trabalhe Conosco, CTA final, Rodapé).

**Seções adicionadas**: nenhuma.

**CTAs**: "Conheça o Projeto de Expansão", "Quem Somos" (hero); "Conhecer nossa história"; "Ver mapa completo"; "Conhecer o modelo de expansão"; "Indicar imóvel"; "Ser fornecedor"; "Ver vagas"; "Falar com a Sol Magazine"; "Conhecer a Expansão" (CTA final).

**Formulários**: nenhum.

**Componentes especiais**: galeria de 2 imagens lado a lado; barra de indicadores em versão clara (`stats-bar light`).

---

## QUEM SOMOS

**Seções existentes**:
1. Hero institucional
2. Origem e Propósito (texto + imagem)
3. Linha do Tempo (4 marcos)
4. Galeria institucional (4 imagens)
5. Escala atual (barra de indicadores)
6. CTA de relacionamento
7. Rodapé

**Seções removidas**: nenhuma frente ao briefing.

**Seções adicionadas**: nenhuma.

**CTAs**: "Ver linha do tempo" (hero, âncora interna); "Falar com a Sol Magazine" (CTA final).

**Formulários**: nenhum.

**Componentes especiais**: timeline vertical com 4 marcos (3 com placeholder, 1 com dado real "+100 lojas... 14 estados"); galeria de 4 imagens em grade.

---

## PRESENÇA NACIONAL

**Seções existentes**:
1. Hero (sem CTA)
2. Mapa do Brasil (placeholder)
3. Presença por Região (4 cards: Norte, Nordeste, Centro-Oeste, Sudeste/Sul)
4. Tabela por estado (14 linhas, todas com dados placeholder exceto o nome do estado)
5. Galeria contextual (4 imagens)
6. Onde Continuamos Crescendo (texto + CTA)
7. CTA por Perfil (4 blocos)
8. Rodapé

**Seções removidas**: nenhuma frente ao briefing.

**Seções adicionadas**: "Presença por Região" — agrupamento por região (Norte/Nordeste/Centro-Oeste/Sudeste-Sul) não está listado explicitamente no briefing como subseção separada do mapa; foi adicionado para complementar a visualização antes da tabela detalhada.

**CTAs**: "Ver mapa completo" (não se aplica aqui, é destino); "Conhecer o Projeto de Expansão"; 4 CTAs por perfil (Investidor, Proprietário, Fornecedor, Candidato).

**Formulários**: nenhum.

**Componentes especiais**: mapa placeholder (360px, sem interatividade real); tabela responsiva com rolagem horizontal em mobile; grade CTA por Perfil.

---

## EXPANSÃO

**Seções existentes**:
1. Hero (CTA "Acessar Landing de Expansão" — link placeholder)
2. Como Crescemos (texto introdutório)
3. Modelo que Sustenta a Expansão (3 cards: Padronização, Critérios claros, Crescimento sustentável)
4. Como a Expansão Acontece (7 etapas numeradas)
5. Critérios de Expansão (3 cards: Localização, Estrutura do imóvel, Potencial de mercado)
6. O que é o Projeto de Expansão (texto + imagem)
7. CTA para Landing de Expansão (faixa escura — link placeholder)
8. CTA por Perfil (4 blocos)
9. Rodapé

**Seções removidas**: nenhuma — todas as 7 seções do briefing estão presentes, mais o rodapé.

**Seções adicionadas**: nenhuma estrutural; porém o link de saída para a Landing de Expansão **não funciona** (aponta para `#`), o que é uma lacuna de conteúdo, não de estrutura.

**CTAs**: "Acessar Landing de Expansão" (hero, placeholder); "Acessar Landing de Expansão" (CTA final, placeholder); 4 CTAs por perfil.

**Formulários**: nenhum — corretamente, conforme o briefing ("esta página NÃO faz captação").

**Componentes especiais**: lista de 7 steps numerados (1 a 7); grade de critérios; CTA por Perfil.

---

## IMÓVEIS

**Seções existentes**:
1. Hero (CTA "Indicar imóvel" → âncora `#formulario`)
2. Por que indicar um imóvel (3 cards)
3. Perfil do imóvel desejado (4 cards: Localização, Metragem, Estrutura, Documentação)
4. Processo (4 steps numerados)
5. Formulário (nome, telefone, e-mail, estado, cidade, metragem, endereço, mensagem)
6. CTA por Perfil (4 blocos)
7. Rodapé

**Seções removidas**: nenhuma frente ao briefing.

**Seções adicionadas**: nenhuma.

**CTAs**: "Indicar imóvel" (hero); "Enviar indicação" (submit do formulário); 4 CTAs por perfil.

**Formulários**: sim — campos: Nome completo*, Telefone*, E-mail*, Estado (select com os 14 estados atendidos), Cidade, Metragem aproximada, Endereço do imóvel, Mensagem. Envio simulado (sem backend), com mensagem de sucesso exibida via JavaScript.

**Componentes especiais**: select de estado pré-populado com os 14 estados oficiais da rede; mensagem de confirmação de envio.

---

## FORNECEDORES

**Seções existentes**:
1. Hero (CTA "Quero ser fornecedor" → âncora `#formulario`)
2. Por que fornecer para a Sol Magazine (3 cards)
3. Categorias compradas (4 cards: Confecções e Moda Popular, Utilidades, Cama/Mesa/Banho, Acessórios)
4. Critérios de homologação (3 cards)
5. Processo (4 steps numerados)
6. Formulário (empresa, CNPJ, responsável, telefone, e-mail, categoria, mensagem)
7. CTA por Perfil (4 blocos)
8. Rodapé

**Seções removidas**: nenhuma frente ao briefing.

**Seções adicionadas**: nenhuma.

**CTAs**: "Quero ser fornecedor" (hero); "Enviar cadastro" (submit); 4 CTAs por perfil.

**Formulários**: sim — campos: Nome da empresa*, CNPJ*, Responsável*, Telefone*, E-mail*, Categoria (select com as 4 categorias oficiais), Mensagem. Envio simulado.

**Componentes especiais**: select de categoria com as 4 categorias exatas do briefing.

---

## TRABALHE CONOSCO

**Seções existentes**:
1. Hero (CTA "Candidatar-se" → âncora `#formulario`)
2. Como é trabalhar aqui (texto introdutório)
3. Áreas de atuação (4 cards: Loja, Logística, Administrativo, Expansão)
4. Histórias de crescimento (3 cards, todos com placeholder de depoimento)
5. Processo seletivo (4 steps numerados)
6. Formulário de candidatura (nome, telefone, e-mail, cidade/estado, área de interesse, currículo, mensagem)
7. CTA compacto ("Ainda não encontrou a vaga ideal?" → "Fale com nosso RH")
8. Rodapé

**Seções removidas**: nenhuma estrutural — todas as 7 seções do briefing estão presentes.
**Atenção**: o briefing pede explicitamente "sem mapa, sem repetição de credenciais institucionais" — o mapa de fato não existe nesta página, mas a barra de credibilidade (+100 lojas / 14 estados / +10 anos) **continua aparecendo no rodapé**, pois o rodapé é um componente global idêntico em todas as páginas. Ver `DIFERENCAS_DO_WIREFRAME.md`, seção 2.

**Seções adicionadas**: nenhuma.

**CTAs**: "Candidatar-se" (hero); "Enviar candidatura" (submit); "Fale com nosso RH" (CTA compacto final).

**Formulários**: sim — campos: Nome completo*, Telefone*, E-mail*, Cidade/Estado, Área de interesse (select: Loja, Logística, Administrativo, Expansão), Currículo (upload de arquivo), Mensagem. Envio simulado.

**Componentes especiais**: campo de upload de currículo (`input type="file"`, sem processamento real); CTA final em versão compacta (mais curta que o padrão "CTA Final" das outras páginas).

---

## CONTATO

**Seções existentes**:
1. Hero neutro (overlay reduzido, sem CTA)
2. Canais por assunto (5 cards: Expansão e Investimento, Imóveis, Fornecedores, RH e Carreiras, Contato Geral)
3. Formulário único (nome, e-mail, telefone, assunto, mensagem)
4. Sidebar institucional (endereço, horário, CNPJ — todos placeholder)
5. Redes sociais (3 ícones placeholder: Instagram, LinkedIn, Facebook)
6. Rodapé

**Seções removidas**: nenhuma frente ao briefing.

**Seções adicionadas**: nenhuma.

**CTAs**: nenhum CTA de navegação além do próprio formulário — corretamente, já que esta é a página de destino final dos demais fluxos.

**Formulários**: sim — campo único: Nome completo*, E-mail*, Telefone, Assunto (select com os 5 canais), Mensagem*. Envio simulado.

**Componentes especiais**: hero com overlay reduzido (`hero-neutro`, conforme a diretriz de hero neutro para esta página); layout de duas colunas (formulário + sidebar) que colapsa para 1 coluna em mobile; grade de 5 canais que colapsa de 3 para 2 para 1 coluna conforme a largura da tela.

---

## Resumo cruzado

| Página | Hero c/ CTA | CTA Final (faixa escura) | CTA por Perfil | Formulário |
|---|---|---|---|---|
| Home | Sim | Sim | Não | Não |
| Quem Somos | Sim (âncora) | Sim | Não | Não |
| Presença Nacional | Não | Não | Sim | Não |
| Expansão | Sim (placeholder) | Sim (placeholder) | Sim | Não |
| Imóveis | Sim (âncora) | Não | Sim | Sim |
| Fornecedores | Sim (âncora) | Não | Sim | Sim |
| Trabalhe Conosco | Sim (âncora) | Sim (compacto) | Não | Sim |
| Contato | Não | Não | Não | Sim |
