# Resumo de Aderência aos Wireframes Homologados

> Síntese da `AUDITORIA_DE_ADERENCIA_AOS_WIREFRAMES.md`. Percentuais são uma estimativa qualitativa baseada na proporção e gravidade das divergências encontradas por página, não uma métrica matemática exata.

## Contagem de divergências por gravidade

| Gravidade | Quantidade | Itens |
|---|---|---|
| CRÍTICA | 5 | Menu sem "Oportunidades" (transversal); Overlay do hero fora da faixa (transversal); Imóveis — campo Link Google Maps ausente; Trabalhe Conosco — 3 campos do formulário ausentes; Contato — Hero não usa Alternativa B |
| MÉDIA | 6 | Home — bloco sem rótulo "Relacionamentos Estratégicos"; Expansão — conteúdo do processo divergente; Imóveis — estacionamento não tratado como diferencial; Trabalhe Conosco — indicador "14 estados" ausente; Contato — Razão social ausente |
| PEQUENA | 4 | Barra de credibilidade sem cor própria (transversal); Trabalhe Conosco — História nº2 não genérica; Trabalhe Conosco — página não reduzida em ~35%; Contato — ícone Facebook extra |

**Total de divergências identificadas: 15** (3 transversais + 12 específicas de página).

## Aderência por página

| Página | Estrutura/Conteúdo | Divergências (C/M/P) | Aderência estimada | Esforço de correção |
|---|---|---|---|---|
| Home | Alta | 0C / 1M / 0P | ~90% | Baixo |
| Quem Somos | Alta | 0C / 0M / 0P | ~95% | Baixo |
| Presença Nacional | Alta | 0C / 0M / 0P | ~95% | Baixo |
| Expansão | Média-Alta | 0C / 1M / 0P | ~85% | Médio |
| Imóveis | Média | 1C / 1M / 0P | ~75% | Médio |
| Fornecedores | Alta | 0C / 0M / 0P | ~95% | Baixo |
| Trabalhe Conosco | Média | 1C / 1M / 2P | ~70% | Médio |
| Contato | Média | 1C / 1M / 1P | ~75% | Médio |
| **Transversais (header/footer/CSS global)** | — | 2C / 0M / 1P | — | Médio |

> Observação: as 3 divergências transversais (menu sem "Oportunidades", overlay fora da faixa, cor da barra de credibilidade) afetam **todas as 8 páginas simultaneamente**, pois residem em `styles.css` e nos componentes de header/footer compartilhados. Por isso reduzem a aderência geral mais do que sugeriria sua contagem isolada.

## Aderência geral do site

- **Aderência geral estimada: ~80%**
- Páginas com **maior aderência**: Quem Somos, Presença Nacional, Fornecedores (estrutura e conteúdo praticamente fiéis às versões homologadas, sem divergências CRÍTICAS específicas de página).
- Páginas com **menor aderência**: Trabalhe Conosco e Contato (ambas com divergência CRÍTICA específica, justamente as duas páginas em que o Dossiê foi mais explícito sobre qual é a "versão final homologada" — maior risco reputacional de não seguir o que foi confirmado).
- O maior fator de não-aderência do site como um todo são as **3 divergências transversais**, especialmente o menu sem agrupamento "Oportunidades" e o overlay do hero fora da faixa homologada — ambas CRÍTICAS e replicadas em todas as páginas.

## Esforço de correção geral

- **Esforço estimado: Médio.**
- As correções transversais (menu dropdown, overlay CSS, cor da barra) são localizadas em poucos arquivos (`styles.css`, possivelmente `script.js` para o comportamento do dropdown, e o `<header>`/`<footer>` repetido nas 8 páginas), mas exigem replicação cuidadosa em todos os HTMLs.
- As correções específicas de página (campos de formulário em Imóveis e Trabalhe Conosco, hero de Contato, rótulo em Home, conteúdo de processo em Expansão) são pontuais e de baixo risco técnico, mas dependem de definição de texto/copy final em alguns casos (ex.: texto-modelo da "História nº2").
- Nenhuma divergência encontrada exige redesenho de arquitetura de informação além do menu — é majoritariamente trabalho de ajuste de conteúdo, CSS e formulário.

## Próximos passos sugeridos

1. Validação deste resumo e da auditoria detalhada pelo usuário.
2. Priorização das correções CRÍTICAS (5 itens) antes das MÉDIAS e PEQUENAS.
3. Autorização explícita do usuário para iniciar a fase de correção de código, que está fora do escopo desta auditoria.
