# Plataforma de revisão manual de geocodificação por setor censitário

Abra a plataforma pelo endereço do GitHub Pages deste repositório. Ela roda inteira no navegador:
a base de revisão é aberta só no computador de quem revisa e **não é enviada** a lugar nenhum.

## Conteúdo

- `index.html`: a plataforma.
- `indices/`: índices territoriais do CNEFE 2010 e 2022 (5570 municípios) e a malha oficial de
  setores censitários do IBGE (5572 municípios), 0.90 GB, gerados em 2026-11-18.
  A plataforma baixa sozinha só os municípios da base aberta (lista em `indices/lista.json`).

Os dados do CNEFE e as malhas são públicos (IBGE). Nunca coloque bases de revisão neste repositório:
o site do GitHub Pages é público, e o `.gitignore` bloqueia CSV, Parquet e planilhas para evitar envio por engano.

## Atualizar

Na pasta do projeto: `python plataforma/build.py`, depois `python publicar/montar_github_pages.py`,
depois, nesta pasta, `git add -A`, `git commit -m "Atualiza a plataforma"` e `git push`.
