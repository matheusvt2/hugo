# Instalação e exemplo do HUGO

[ref](https://gohugo.io/getting-started/quick-start/)

## 1. Instalar HUGO

```bash
sudo apt install hugo 
```

## 2. Criar um novo site

```bash
hugo new site meusite --verbose --environment dev -f "yaml"
```

## 3. Adicionar um tema

Existe um site para os temas do HUGO [Hugo Themes](https://themes.gohugo.io/), neste caso usaremos o tema [Ananke](https://themes.gohugo.io/themes/gohugo-theme-ananke/).

```bash
cd meusite
git init
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
git submodule update --init --recursive
```

Após da atualização do submódulo, devemos alterar a configuração do arquivo config.yaml:

```yaml
theme: ananke
defaultcontentlanguage: pt-br
```

## 4. Adicionar algum conteúdo

Podemos adiconar conteúdos criando diretamente páginas no diterório `<nomedosite>`/content/`<ling>`/`<novapagina.md>` ou pelo comando abaixo:

```bash
hugo new content/pt-br/my-first-post.md
```

## 5. Rodar o HUGO server

```bash
hugo server --disableFastRender
```

## 6. Criando um menu e uma página nova

Alterar o arquivo config.yml:

```yaml

```