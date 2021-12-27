# demo mkdocs, mathjax and github-pages

A simple demo `mkdocs`, `material` theme, `mathjax` and `github-pages`.

useful reference

1. [mkdocs.org](https://www.mkdocs.org)
2. [mkdocs-material](https://squidfunk.github.io/mkdocs-material/)

## quickstart

1. `pip install mkdocs-material`
2. `mkdocs new my-project`
3. edit `mkdocs.yml`: see below
4. edit `docs/math.md`: see below
5. `mkdocs serve`: open website `127.0.0.1:8000` to view the doc locally
6. `git init`, `git remote add origin xxx` add github repo url, replace `xxx`
7. `mkdocs gh-deploy`: create a branch `gh-pages` and push to github
8. open website `https://xxx.github.io/yyy/` to view the documentation online, `xxx` should be your github username, `yyy` should be the repo name

`mkdocs.yml`

```yaml
site_name: demo mkdocs, mathjax and github-pages
site_url: https://example.com/
theme:
  name: material
  palette:
    - scheme: default
      toggle:
        icon: material/toggle-switch-off-outline
        name: Switch to dark mode
    - scheme: slate
      toggle:
        icon: material/toggle-switch
        name: Switch to light mode
markdown_extensions:
  - pymdownx.arithmatex:
      generic: true
extra_javascript:
  - javascripts/mathjax.js
  - https://polyfill.io/v3/polyfill.min.js?features=es6
  - https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js
```

`math.md`

```Markdown
# math

inline mode $ax^2+bx+c=0$

$E=mc^2$

is display mode
```

## file layout

```text
.
├── docs/
│   ├── index.md
│   └── math.md
└── mkdocs.yml
```
