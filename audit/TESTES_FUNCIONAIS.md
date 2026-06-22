# Testes Funcionais — Pós-Correção

> Testes executados de forma automatizada (Playwright/Chromium headless) sobre o protótipo HTML servido localmente, após a fase de correções (Etapa 3). Objetivo: validar que as correções implementadas funcionam de fato no navegador, e não apenas no código-fonte.

## 1. Teste do menu desktop

- **O que foi testado**: contagem e rótulos dos itens visíveis no `.nav-links` em viewport desktop (1440×900), na Home.
- **Resultado**: 5 itens visíveis — `Home`, `Quem Somos`, `Presença Nacional`, `Oportunidades`, `Contato`.
- **Status**: ✅ **Passou.** O menu deixou de exibir 8 itens planos e passou a refletir o agrupamento homologado (3 itens diretos + "Oportunidades" + Contato).

## 2. Teste do dropdown "Oportunidades"

- **O que foi testado**: hover sobre o item "Oportunidades" (desktop) e verificação de que o submenu fica visível, com os 4 itens esperados; em seguida, clique em um item do submenu para confirmar navegação.
- **Resultado**:
  - Submenu visível ao passar o mouse: `true`.
  - Itens do submenu: `Expansão`, `Imóveis`, `Fornecedores`, `Trabalhe Conosco` (na ordem correta).
  - Clique em "Imóveis" navegou corretamente para `imoveis.html`.
- **Status**: ✅ **Passou.**

## 3. Teste do menu mobile

- **O que foi testado**: viewport mobile (390×844), estado inicial do menu (fechado), clique no botão hambúrguer (`.menu-toggle`) para abrir o menu, e clique no item "Oportunidades" para expandir o submenu dentro do menu mobile.
- **Resultado**:
  - Estado antes do toque: menu fechado (`open=false`).
  - Estado após o toque no hambúrguer: menu aberto (`open=true`).
  - Após tocar em "Oportunidades": submenu expandido (`open=true` na `li.has-dropdown`) e o link "Expansão" ficou visível e clicável dentro do submenu.
- **Status**: ✅ **Passou.** O comportamento de toque (em vez de hover, inadequado para mobile) funciona conforme implementado em `script.js`.

## 4. Teste dos links entre páginas

- **O que foi testado**: em cada uma das 8 páginas, foi coletado todo link interno (`href` terminando em `.html`) e feita uma requisição HTTP para confirmar resposta `200`.
- **Resultado**: todos os links internos das 8 páginas (incluindo header, dropdown, footer, CTAs e cards de perfil) retornaram **status 200** — nenhum link quebrado encontrado.
- **Status**: ✅ **Passou.**

## 5. Teste dos formulários visuais

- **O que foi testado**: para os 4 formulários alterados/relevantes (Imóveis, Fornecedores, Trabalhe Conosco, Contato), foi verificada a presença de todos os campos esperados (rótulos) e, em seguida, simulado um preenchimento mínimo dos campos obrigatórios seguido de envio, confirmando a exibição da mensagem de sucesso do protótipo (`.form-success`).
- **Resultado**:
  - **Imóveis**: todos os 10 campos esperados presentes, incluindo os novos "Possui estacionamento (diferencial, não obrigatório)" e "Link Google Maps (opcional)". Envio simulado exibiu mensagem de sucesso.
  - **Fornecedores**: todos os 7 campos esperados presentes (sem alteração nesta fase). Envio simulado exibiu mensagem de sucesso.
  - **Trabalhe Conosco**: todos os 10 campos esperados presentes, incluindo "Cidade Atual", "Disponibilidade para Mudança", "Disponibilidade para Início" e "Experiência". Envio simulado exibiu mensagem de sucesso.
  - **Contato**: todos os 5 campos esperados presentes (sem alteração estrutural nesta fase, apenas o hero). Envio simulado exibiu mensagem de sucesso.
- **Status**: ✅ **Passou** nos 4 formulários testados.

## 6. Teste do link para a Landing de Expansão

- **O que foi testado**: os dois pontos de CTA na página Expansão que apontam para a Landing de Expansão (hero, `#link-landing-expansao`, e CTA final, `#link-landing-expansao-2`).
- **Resultado**: ambos os links têm `href="#"` — são placeholders, como já sinalizado visualmente no protótipo (`<span class="placeholder-tag">URL placeholder</span>` no CTA final).
- **Status**: ⚠️ **Esperado/não é regressão.** A URL real da Landing de Expansão depende de um projeto separado (confirmado no Dossiê Oficial — "a Landing de Expansão é projeto separado"). Este teste apenas documenta que o placeholder continua ativo e funcional como placeholder; não é uma falha introduzida pelas correções desta fase.

## Pendências encontradas

| # | Pendência | Origem | Gravidade | Ação recomendada |
|---|---|---|---|---|
| 1 | Links da Landing de Expansão (`#link-landing-expansao`, `#link-landing-expansao-2`) permanecem com `href="#"` | Pré-existente, fora do escopo da auditoria de aderência | Não é divergência de wireframe — é dado de produção pendente | Atualizar a URL real quando a Landing de Expansão for publicada |
| 2 | M2 (Expansão) — o texto revisado da seção "Como a Expansão Acontece" foi escrito com base nos critérios do Dossiê Oficial, sem acesso direto às imagens 6–12 do wireframe v2 nesta fase | Já sinalizado em `RELATORIO_CORRECOES_EXECUTADAS.md` | Baixa | Validação fina de copy contra o wireframe v2 original |

Nenhuma outra pendência funcional foi encontrada: menu, dropdown, navegação entre páginas e formulários funcionam corretamente em desktop e mobile.
