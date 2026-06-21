# Diferenças do Wireframe — Protótipo HTML vs. Especificação Homologada

> Base de comparação: o briefing institucional consolidado (Fase 2) fornecido como especificação homologada. Não há arquivos de wireframe (Figma/PDF/imagem) anexados ao repositório — a comparação abaixo é feita entre **o texto da especificação aprovada** e **o HTML efetivamente implementado**. Nenhuma divergência identificada foi omitida.

## 1. Alterações Visuais

- **Fotos de hero**: a especificação exige "foto protagonista obrigatória, sempre visível". Na implementação, todos os heros usam uma imagem placeholder de cor sólida (`https://placehold.co/1600x900/...`), pois não há fotos reais disponíveis. Visualmente, o hero hoje **não tem foto real**, apenas um bloco de cor — a regra de "foto sempre visível, overlay só atrás do texto" foi implementada estruturalmente (gradiente lateral), mas não pode ser validada visualmente sem a foto real.
- **Overlay do hero**: implementado como gradiente (`90deg`) que vai de ~84% de opacidade perto do texto até 0% do lado oposto, e não como um overlay de opacidade fixa única (32–42%) cobrindo uma área plana. Tecnicamente atende ao espírito da regra ("nunca ocultar a foto", "overlay só atrás do bloco textual"), mas a curva de gradiente é uma interpretação livre da faixa 32–42% mencionada no briefing, já que não havia wireframe pixel-a-pixel para seguir.
- **Vermelho institucional**: foi definido um valor específico (`#c41e1e`, com variante escura `#9c1818`). O briefing não define o hex exato — esta é uma decisão de implementação, não uma divergência, mas fica registrada por não haver wireframe/manual de marca para validar o tom exato.
- **Rodapé**: cor `#271414` aplicada exatamente como especificado.
- **Indicadores**: regra "fundos escuros = texto branco, fundos claros = vermelho institucional" foi implementada via duas variantes de classe CSS (`.stats-bar` e `.stats-bar.light`).
- **Badges, CTAs, bordas**: todos em vermelho institucional, sem grandes blocos vermelhos de fundo — em conformidade com a diretriz.

## 2. Alterações Estruturais

- **Página Expansão**: a especificação afirma que existe uma **Landing Page de Expansão separada** e que a página institucional "não faz captação, apenas direciona". Na implementação, **essa Landing Page não existe** — os dois pontos de saída (hero e CTA final) são links `href="#"` com a tag de placeholder "URL placeholder". Isso é uma divergência estrutural relevante: o fluxo de captação real está incompleto até a URL ser fornecida.
- **Página Trabalhe Conosco**: a especificação determina explicitamente "sem mapa, sem repetição de credenciais institucionais". A implementação segue essa regra na seção principal, mas o **rodapé** (compartilhado por todas as páginas) repete a barra de credibilidade (+100 lojas / 14 estados / +10 anos) também nesta página. Tecnicamente isso é repetição de credenciais institucionais, ainda que apenas no rodapé padrão — não há uma versão "simplificada" do rodapé para essa página.
- **Seção "CTA por Perfil"**: presente em 4 das 8 páginas (Presença Nacional, Expansão, Imóveis, Fornecedores), mas ausente em Home, Quem Somos, Trabalhe Conosco e Contato. O briefing não detalha em quais páginas esse padrão deveria aparecer — a distribuição atual é uma decisão de implementação, não uma instrução explícita do briefing.
- **CTA Final (faixa escura)**: presente em Home, Quem Somos, Expansão e Trabalhe Conosco, mas ausente em Presença Nacional, Imóveis, Fornecedores e Contato — mesma observação acima.

## 3. Alterações de Conteúdo

- **Quantidade de lojas por estado / municípios atendidos**: a especificação already prevê isso como "dado pendente, usar placeholder". Implementado como placeholder textual (`—` + tag) na tabela de Presença Nacional, conforme instruído.
- **CNPJ, razão social, endereço, horário, e-mails, handles de Instagram**: todos implementados como placeholders identificados visualmente (tag vermelha "placeholder"), conforme a diretriz de "usar placeholders claramente identificados".
- **Fotos reais**: substituídas por blocos de cor com rótulo textual indicando o tipo de imagem esperada (ex.: "Foto institucional", "Foto de loja") — não há nenhuma imagem fotográfica real no protótipo.
- **Histórias reais de colaboradores** (Trabalhe Conosco): implementadas como 3 cards genéricos com texto "Depoimento real a ser inserido na versão final" — nenhum depoimento real foi criado nem inventado.
- **URL da Landing de Expansão**: ausente, como descrito na seção estrutural acima.

## 4. Alterações Mobile

- **Menu mobile**: o briefing não especifica o comportamento exato do menu em telas pequenas. Foi implementado um menu "hambúrguer" com painel deslizante (`max-height` animado) que empilha os 8 itens verticalmente. O botão fixo "Fale Conosco" é **ocultado** no mobile (abaixo de 920px) — author decision para evitar redundância com o item "Contato" já presente na lista, mas isso significa que o CTA fixo de conversão não está disponível no mobile, apenas dentro do menu expandido.
- **Grids responsivos**: todas as grades de 2, 3 e 4 colunas colapsam para 1 coluna em telas ≤920px (ou 2 colunas em alguns casos intermediários, como a galeria). Não há um breakpoint intermediário "tablet" tratado de forma diferenciada — o salto é direto de desktop para mobile em 920px.
- **Tabela de estados (Presença Nacional)**: em mobile, a tabela usa rolagem horizontal (`overflow-x: auto`) em vez de uma reformatação em cards — decisão de implementação não detalhada no briefing.
- **Formulários**: campos em grade 2 colunas no desktop colapsam para 1 coluna em mobile (≤700px).

## 5. Alterações de Navegação

- **Dropdowns**: o briefing não menciona dropdowns, e nenhum foi implementado. O menu é uma lista plana de 8 itens. Caso a arquitetura de informação homologada previsse algum agrupamento (ex.: um dropdown "Oportunidades" reunindo Imóveis/Fornecedores/Trabalhe Conosco), isso **não está implementado** — sinalizado aqui por não haver wireframe disponível para confirmar.
- **Página ativa no menu**: destaque visual do item ativo implementado via JavaScript (comparação de URL), não estava descrito no briefing — decisão de implementação para UX de navegação.
- **Âncoras internas**: várias páginas usam links internos por âncora (`#formulario`, `#linha-do-tempo`) para CTAs do hero — mecanismo de navegação não mencionado no briefing, mas necessário para um protótipo de página única navegável sem JavaScript de roteamento.
- **Landing de Expansão**: como já indicado, o link existe mas não navega para lugar nenhum (âncora vazia `#`) — maior divergência de navegação do protótipo.

## Resumo de criticidade

| Divergência | Criticidade | Motivo |
|---|---|---|
| Landing de Expansão inexistente | Alta | Fluxo de captação primário de investidores incompleto |
| Rodapé repete credenciais em Trabalhe Conosco | Baixa | Contradiz instrução explícita de "página simplificada", mas é comportamento do componente global de rodapé |
| Overlay de hero como gradiente, não opacidade plana | Média | Interpretação livre de uma regra numérica (32–42%) sem wireframe de referência |
| Ausência de dropdowns | A confirmar | Sem wireframe para validar se isso era esperado |
| Distribuição não padronizada de CTA Final / CTA por Perfil | Baixa | Decisão de implementação sem instrução explícita por página |
| Fotos/depoimentos reais ausentes | Esperado | Já previsto no briefing como dado pendente |
