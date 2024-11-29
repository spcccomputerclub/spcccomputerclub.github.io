# spcccomputerclub.github.io

Crappy Static site generation.

## Specs

### Folder structure
```
branches
├── main
└── gh-pages
```
`main` is the where everything at, and `gh-pages` is public for deployment

#### The `main` branch
```
branches/main
├── content/
│   └── markdowns/
├── dist/
├── scripts/
│   └── generate_pages.py
├── template/
│   └── assets/
├── config.toml
├── LICENSE
└── requirements.txt
```
- `content/markdown/`: Markdown files to include in spcccomputerclub.github.io/articles
- `template/`: Boilerplate files and assets, raw material for site generation.
    - `template/assets/`: the entire directory will be copied to `/dist/` 
- `scripts/generate_pages.py`: Main program
- `dist`: Generated site, ready for deploy. This subdirectory is also mounted to the root of `branches/gh-pages`
The [https://github.com/spcccomputerclub/spcccomputerclub.github.io/blob/main/.github/workflows/main.yml](workflow) will automatically run `scripts/generate_pages.py` and copy the content in `dist/` to `branches/gh-pages`

### Upload new article
As previously mentioned, the workflow will automatically execute the site generation after each push to the repository.
1. In `content/markdown/`, create a new folder `[TITLE].d`.
```
/content/markdown/[TITLE].d
├── article.md
└── meta.toml
```
In `meta.toml`, include the following information:
```toml
id = "0001" # Give it a unique ID
title = "Insert Title here" # Title
date = 1979-05-27 # Date in YYYY-MM-DD format
author = "James" # Author
# Tags
tags = [
    "SSD",
    "Data Storage",
    "Technology Guide",
    "Computer Hardware",
    "AI-generated",
]
draft = false # This one is not yet implemented
thumbnail = "logo.jpg" # Path of the thumbnail. Has the prefix `/template/assets/image/`
```
2. In `articles.md`, include the main article. Do not include the main title as it will be automatically added to the page.
```markdown
## Lorem Ipsum
Lorem ipsum dolor sit amet.
.. toc::
```
> [!NOTE]
> The markdown parser in the site generation process will automatically insert a table of content at `.. toc::`

#### Include assets in the article
The parser directly passes the links into html. For example:
```markdown
![Normal Mouse](/assets/img/0001/normalmouse.png)
```
Will turn into:
```html
<img src="/assets/img/0001/normalmouse.png" />
```
and access [spcccomputerclub.github.io/assets/img/0001/normalmouse.png](spcccomputerclub.github.io/assets/img/0001/normalmouse.png), aka `branches/main/template/assets/img/0001/normalmouse.png`
