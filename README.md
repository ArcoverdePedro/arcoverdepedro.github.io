# GreenArch — Portfólio de Pedro Arcoverde

Site estático bilíngue desenvolvido **somente com HTML e CSS**. Sem JavaScript, Astro, Node.js, build ou dependências.

## Arquivos

- `index.html`: página em português
- `en/index.html`: página em inglês
- `css/style.css`: design e animações compartilhados
- `public/favicon.svg`: marca GreenArch
- `public/profile.jpg`: fotografia de perfil original (usada no `og:image`)
- `public/profile-{360,720}.{avif,webp,jpg}`: versões otimizadas exibidas no site
- `CNAME`: domínio `greenarch.com.br`
- `.nojekyll`: impede processamento pelo Jekyll

## Execução local

Abra `index.html` em um servidor estático simples (não diretamente via `file://`, pois os caminhos dos assets começam em `/`).

Exemplo com Python, sem instalação de pacotes:

```sh
python3 -m http.server 8000
```

Abra `http://localhost:8000/` e `http://localhost:8000/en/`.

## Publicação

O GitHub Actions publica diretamente os arquivos na raiz do repositório, sem etapa de compilação. O GitHub Pages deve permanecer configurado com **Source: GitHub Actions**. As URLs PT e EN são caminhos independentes e não exigem JavaScript.

Para atualizar os textos, edite as duas páginas HTML. Para alterar o visual, edite apenas `css/style.css`.
