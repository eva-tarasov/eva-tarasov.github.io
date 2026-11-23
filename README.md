# eva-tarasov.github.io

Личный блог: https://eva-tarasov.github.io — [Hugo](https://gohugo.io) + тема [PaperMod](https://github.com/adityatelange/hugo-PaperMod).

## Как устроено
- `content/posts/<slug>/index.md` — статья; картинки лежат рядом в той же папке (page bundle).
- `content/about.md` — страница «Обо мне», `hugo.toml` — настройки сайта и меню.
- `themes/PaperMod` — тема (git submodule). Клонировать с ней: `git clone --recursive …`
  или после клона `git submodule update --init`.
- `.github/workflows/pages.yml` — на каждый push в `main` собирает сайт и публикует на GitHub Pages.

## Локально
```bash
brew install hugo
hugo server -D        # http://localhost:1313, -D показывает и черновики (draft: true)
```

## Новая статья
```bash
hugo new content posts/my-post/index.md   # создаётся с draft: true
```
Публикация — `draft: false` и push в `main`.
