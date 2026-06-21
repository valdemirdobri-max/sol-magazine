# Arquitetura do Site — Protótipo HTML Navegável (Fase 2)

> Documento gerado a partir da implementação real (HTML/CSS/JS) entregue no protótipo. Não depende de leitura do código-fonte completo — descreve a estrutura observável e navegável do site.

## 1. Estrutura completa de páginas

O protótipo contém **8 páginas HTML estáticas**, todas interligadas pelo mesmo cabeçalho e rodapé:

| Arquivo | Página |
|---|---|
| `index.html` | Home |
| `quem-somos.html` | Quem Somos |
| `presenca-nacional.html` | Presença Nacional |
| `expansao.html` | Expansão |
| `imoveis.html` | Imóveis |
| `fornecedores.html` | Fornecedores |
| `trabalhe-conosco.html` | Trabalhe Conosco |
| `contato.html` | Contato |

Não existe Landing Page de Expansão separada no protótipo — a página `expansao.html` contém apenas **um link placeholder** (`#`) com texto "Acessar Landing de Expansão", já que a URL definitiva ainda não foi fornecida.

## 2. Menu principal

Menu fixo (`sticky`) no topo de todas as páginas, com a seguinte ordem:

1. Home
2. Quem Somos
3. Presença Nacional
4. Expansão
5. Imóveis
6. Fornecedores
7. Trabalhe Conosco
8. Contato

Ao lado do menu, há um botão de destaque (CTA) fixo: **"Fale Conosco"**, que leva sempre para `contato.html`.

O item de menu correspondente à página atual recebe destaque visual (sublinhado e cor vermelha) via JavaScript (`script.js`), comparando a URL atual com o `href` de cada link.

## 3. Dropdowns

**Não há dropdowns no menu.** A navegação principal é uma lista plana de 8 itens — não há submenus, mega menus ou agrupamento hierárquico. Isso é uma decisão de implementação tomada diante da ausência de menção a dropdowns no briefing homologado.

## 4. Fluxos de navegação

Fluxos identificados na implementação:

- **Home → todas as demais páginas**: a Home contém blocos de resumo (Quem Somos, Presença Nacional, Expansão) e cards de chamada (Imóveis, Fornecedores, Trabalhe Conosco), cada um levando à respectiva página.
- **Qualquer página → Contato**: via botão fixo "Fale Conosco" no menu e via blocos de "CTA por Perfil" presentes ao final da maioria das páginas.
- **Presença Nacional → Expansão**: bloco "Onde Continuamos Crescendo" linka para a página de Expansão.
- **Expansão → Landing de Expansão (externa)**: dois pontos de saída (hero e CTA final) apontam para um link placeholder, pois a URL real não existe ainda.
- **Imóveis / Fornecedores / Trabalhe Conosco**: cada uma contém um formulário interno (âncora `#formulario`) acessado por um botão no hero ("Indicar imóvel", "Quero ser fornecedor", "Candidatar-se").
- **Contato**: ponto de convergência final, com canais segmentados por assunto e formulário único.
- **Navegação cruzada por "CTA por Perfil"**: presente em Presença Nacional, Expansão, Imóveis e Fornecedores — sempre oferecendo 4 caminhos (Investidor → Expansão, Proprietário → Imóveis, Fornecedor → Fornecedores, Candidato → Trabalhe Conosco), exceto quando a própria página já é um desses destinos (nesse caso ela é substituída por "Geral → Contato").

## 5. CTAs existentes

CTAs mapeados por tipo:

**CTA fixo (em todas as páginas)**
- "Fale Conosco" (menu) → `contato.html`

**CTAs de Hero (por página)**
- Home: "Conheça o Projeto de Expansão", "Quem Somos"
- Quem Somos: "Ver linha do tempo" (âncora interna)
- Presença Nacional: nenhum CTA no hero (apenas texto institucional)
- Expansão: "Acessar Landing de Expansão" (placeholder)
- Imóveis: "Indicar imóvel" (âncora `#formulario`)
- Fornecedores: "Quero ser fornecedor" (âncora `#formulario`)
- Trabalhe Conosco: "Candidatar-se" (âncora `#formulario`)
- Contato: nenhum CTA no hero (hero neutro, sem ação)

**CTAs de seção**
- Home: "Conhecer nossa história", "Ver mapa completo", "Conhecer o modelo de expansão", "Indicar imóvel", "Ser fornecedor", "Ver vagas"
- Quem Somos: "Falar com a Sol Magazine"
- Presença Nacional: "Conhecer o Projeto de Expansão"
- Trabalhe Conosco: "Fale com nosso RH"

**CTA Final (faixa de destaque, fundo escuro)**
- Presente em: Home, Quem Somos, Expansão, Trabalhe Conosco (versão compacta)
- Ausente em: Presença Nacional (substituída por CTA por Perfil), Imóveis, Fornecedores (idem), Contato (página é o próprio destino final)

**CTA por Perfil (grade de 4 blocos)**
- Presente em: Presença Nacional, Expansão, Imóveis, Fornecedores
- Ausente em: Home, Quem Somos, Trabalhe Conosco, Contato

**CTAs de formulário (botões de envio)**
- "Enviar indicação" (Imóveis)
- "Enviar cadastro" (Fornecedores)
- "Enviar candidatura" (Trabalhe Conosco)
- "Enviar mensagem" (Contato)

## 6. Componentes reutilizados

Componentes compartilhados entre páginas (definidos uma vez em `styles.css` e replicados via marcação HTML idêntica em cada página):

| Componente | Onde aparece |
|---|---|
| Cabeçalho (`site-header`) com menu sticky | Todas as páginas |
| Hero com overlay gradiente (32–42% atrás do texto) | Todas as páginas |
| Barra de indicadores (`stats-bar`) — +100 lojas / 14 estados / +10 anos | Home, Quem Somos, Presença Nacional, rodapé de todas as páginas |
| Cards (`card`) | Home, Presença Nacional, Expansão, Imóveis, Fornecedores, Trabalhe Conosco |
| Steps numerados (`steps`) | Expansão (7 etapas), Imóveis, Fornecedores, Trabalhe Conosco |
| Timeline vertical | Quem Somos (linha do tempo) |
| Galeria de imagens em grade | Home, Quem Somos, Presença Nacional |
| Tabela responsiva de estados | Presença Nacional |
| Mapa placeholder | Presença Nacional |
| Bloco CTA Final (faixa escura) | Home, Quem Somos, Expansão, Trabalhe Conosco |
| Grade "CTA por Perfil" (4 blocos) | Presença Nacional, Expansão, Imóveis, Fornecedores |
| Formulário padrão (`form-card` + `form-grid`) | Imóveis, Fornecedores, Trabalhe Conosco, Contato |
| Mensagem de sucesso de formulário (`form-success`) | Imóveis, Fornecedores, Trabalhe Conosco, Contato |
| Rodapé completo (`site-footer`) com barra de credibilidade #271414 | Todas as páginas |
| Tag de placeholder visual (`placeholder-tag`) | Onde há dado institucional pendente |

Todos os componentes compartilham o mesmo arquivo `styles.css` (CSS único, sem pré-processador) e o mesmo `script.js`, responsável por: menu mobile, destaque do item de menu ativo, animação de entrada (fade-in) e simulação de envio de formulário (sem backend real).
