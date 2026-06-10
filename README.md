# Portfólio — Alexandre Soares

Este repositório contém um site de portfólio estático, focado em apresentar projetos, serviços e informações de contato de forma simples e responsiva.

O layout é em tema escuro com destaques em neon, inclui versões desktop e mobile, e um redirecionamento simples que leva usuários móveis a uma versão dedicada.

<a href="https://cl3af.netlify.app">Deploy do portfólio rodando</a> 

## Estrutura principal

- `index.html` — Página inicial (desktop)
- `github.html` — Página com link para o perfil GitHub (desktop)
- `portfolio.html` — Lista de projetos (desktop)
- `services.html` — Serviços e preços (desktop)
- `githubMobile.html`, `portfolioMobile.html`, `servicesMobile.html` — Versões simplificadas para dispositivos móveis
- `menuMobile.html` — Menu/entrada para a versão mobile
- `css/styles.css` — Estilos do site (variáveis CSS, componentes, responsividade)
- `img/` — Imagens usadas no site (ex.: `logo-projeto1.jpg`)

## Funcionalidades e detalhes técnicos

- Redirecionamento mobile: cada página desktop contém um script que redireciona para `menuMobile.html` quando `window.innerWidth < 640`.
- Estilos principais estão em `css/styles.css` com variáveis (`--bg`, `--neon`, `--text`) para facilitar personalização.
- Componentes notáveis no CSS:
  - `.thumb` — área de imagem dos projetos, com `overflow: hidden` e `img { object-fit: cover }` para manter proporção.
  - `.nav-list a` — botões do menu com borda arredondada e animação de hover (translateY + box-shadow).
  - Regras de responsividade (`@media (max-width:640px)` e `@media (min-width:800px)`) para ajustar layout e grid de projetos.

## Como usar localmente

1. Clone o repositório:

```bash
git clone https://github.com/cl3af/portfolio.git
cd portfolio
```

2. Abra os arquivos `.html` diretamente no navegador ou use um servidor local:

```bash
# Com Python 3
python -m http.server 8000

# Ou com Node (http-server)
npx http-server

# Acesse: http://localhost:8000
```

3. Para testes mobile abra as páginas `*Mobile.html` ou redimensione a janela para <640px e deixe o script redirecionar.

## Como editar / adicionar conteúdo

- Para adicionar um projeto, edite `portfolio.html` e `portfolioMobile.html` adicionando um novo `<article class="project">` com uma imagem em `img/` e descrição.
- Para mudar cores, edite as variáveis em `css/styles.css` no seletor `:root`.
- Para ajustar o comportamento mobile, altere o valor do breakpoint no script (atualmente 640px) ou converta o redirecionamento para uma abordagem baseada em CSS/JS mais avançada.

## Boas práticas / sugestões

- Adicione um arquivo `.gitignore` para evitar enviar arquivos do OneDrive e do sistema:

```
# Exemplo mínimo
.DS_Store
node_modules/
.env
Thumbs.db
*.tmp
```

- Use GitHub Pages, Netlify ou Vercel para hospedar facilmente o site estático.

## Histórico de alterações (local)

- 2026 — Criação do site, adição de versões mobile e ajustes de estilo.

## Contato

- Autor: Alexandre Soares
- GitHub: https://github.com/cl3af

---

_README gerado / atualizado localmente para documentar o projeto._
