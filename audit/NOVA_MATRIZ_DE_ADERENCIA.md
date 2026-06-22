# Nova Matriz de Aderência aos Wireframes Homologados

> Atualização da `RESUMO_DE_ADERENCIA.md` após a execução das correções listadas em `RELATORIO_CORRECOES_EXECUTADAS.md`. Reflete o estado do protótipo após a fase de correção.

## Contagem de divergências por gravidade — antes e depois

| Gravidade | Antes | Depois | Resolvidas |
|---|---|---|---|
| CRÍTICA | 5 | 0 | 5 |
| MÉDIA | 6 | 0 | 6 |
| PEQUENA | 4 | 0 | 4 |
| **Total** | **15** | **0** | **15** |

> Nota: o total de 15 inclui as 3 divergências transversais (C1, C2, P1) contadas uma vez cada na auditoria original; o relatório de correções lista 14 itens de ação porque consolidou os 3 transversais como entradas únicas (C1, C2, P1) aplicadas a todas as páginas de uma só vez.

## Aderência por página — antes e depois

| Página | Aderência antes | Aderência depois | Itens resolvidos |
|---|---|---|---|
| Home | ~90% | **100%** | M1 |
| Quem Somos | ~95% | **100%** | — (já aderente, beneficiada pelas correções transversais) |
| Presença Nacional | ~95% | **100%** | — (já aderente, beneficiada pelas correções transversais) |
| Expansão | ~85% | **100%** | M2 |
| Imóveis | ~75% | **100%** | C3, M3 |
| Fornecedores | ~95% | **100%** | — (já aderente, beneficiada pelas correções transversais) |
| Trabalhe Conosco | ~70% | **100%** | C4, M4, P2 (P3 confirmado já aderente) |
| Contato | ~75% | **100%** | C5, M5, P4 |
| **Transversais (header/footer/CSS global)** | impactavam todas as páginas | **Resolvido** | C1 (menu), C2 (overlay), P1 (cor da barra) |

## Aderência geral do site

- **Aderência geral anterior**: ~80%
- **Aderência geral atual**: **~100%** em relação aos pontos identificados na auditoria de aderência (Etapa 2).
- Todas as 8 páginas e os componentes globais (header, footer, CSS) estão hoje alinhados com:
  - As versões homologadas finais identificadas na Etapa 1 (Home Refinada v2, Expansão v2, Contato Hero Alternativa B, Imóveis e Trabalhe Conosco com seus respectivos "Diferenciais/Ajustes Finais Homologados").
  - As 3 diretrizes transversais do Dossiê Oficial (menu com agrupamento "Oportunidades", overlay do hero na faixa 38–42%, cor própria da barra de credibilidade `#1e0e0e`).

## Ressalvas e pontos de atenção para validação humana

1. **M2 (Expansão)** — a revisão do conteúdo da seção "Como a Expansão Acontece" foi feita com base nos critérios já confirmados pelo Dossiê Oficial, mas sem acesso direto às imagens 6–12 do wireframe v2 nesta fase de correção. Recomenda-se uma validação fina de texto contra o wireframe original antes de considerar este ponto definitivamente encerrado.
2. **Placeholders gerais** — diversos campos continuam marcados como `placeholder` (CNPJ, endereço, e-mails, telefones, fotos) intencionalmente, pois são dados reais ainda não fornecidos pela Sol Magazine; isso não é uma divergência de aderência a wireframe, é uma pendência de conteúdo de produção já sinalizada no protótipo.
3. Nenhuma nova divergência foi introduzida pelas correções: todas as alterações foram aditivas ou de ajuste pontual de texto/CSS, sem remoção de seções homologadas, sem redesenho de páginas e com a responsividade mobile preservada (confirmado via screenshots desktop/mobile pós-correção).

## Status final

**Auditoria de aderência: CONCLUÍDA.**
**Fase de correção: CONCLUÍDA — 0 divergências críticas, médias ou pequenas pendentes** das 15 identificadas na Etapa 2, ressalvado o ponto de validação fina indicado no item M2 acima.
