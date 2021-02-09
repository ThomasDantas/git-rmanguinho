# Treinamento sobre GIT - Rodrigo Manguinho

> Link: https://www.youtube.com/playlist?list=PL9aKtVrF05DzbNiE7jcm7s6z6Lg-u72Rq

---

- `workspace` = conteudo local;
- `remote repository` = nuvem / clonar para a maquina;

---

## Comandos - Aula 1

    --------------- INIT ------------------
    $ git init // iniciar repositorio local

    --------------- CLONE ------------------
    $ git clone // clonar um repositorio

    --------------- REMOTE -V ------------------
    $ git remote -v // mostra repositorios remotos

    --------------- REMOTE ADD ------------------
    $ git add remote add (apelido, ex: origin) (url) // adicionar repositorio remoto

    --------------- CONFIG SYSTEM ------------------
    $ git config --system --edit // config do sistema

    --------------- CONFIG USER ------------------
    $ git config --global --edit // config do usuario

     --------------- CONFIG LOCAL ------------------
    $ git config --local --edit // config local projeto

    --------------- CONFIGS OPEN VSCODE ------------------
    $ git config --global core.editor code // abrir configs no vscode

---

## Comandos - Aula 2

      --------------- COMMIT ------------------
    $ git status // arquivos modificados (M - modificado, A - adicionado, ? - desconhecido)

    $ git add (fileName) ou (.) // . adiciona otodos

    $ git add --all // adicionar todos os arquivos de todos os diretorios

    $ git commit -m "mensagem" // mensagem a ser commitada

    $ git commit --amend --no-edit // commitado junto ao comite anterior

    $ git log // mostra todos os commits

    $ git stash // voltar para como estava no ultimo commit

    $ git stash list // mostra lista de stash

    $ git stash pop // voltar para para not staged, e remove do stash

    $ git stash clear // limpa stash

- Criar atalhos (alias)

      --------------- ALHIAS ------------------
      $ git config --global --edit // configs pessoais do usuario

      [user]
        name = your_name
        email = your_email
      [credential]
        helper = store
      [core]
        editor = code
      [alias]
        s = !git status -s
        c = !git add --all && git commit -m

        $ git s // git status -s
        $ git c "message" // adicionar e depois comita

---

## Comandos - Aula 3

> Convetional Commits - https://www.conventionalcommits.org/en/v1.0.0/#summary

1.  `fix:` a commit of the type **_fix_** patches a bug in your codebase (this correlates with PATCH in semantic versioning).

2.  `feat:` a commit of the type **_feat_** introduces a new feature to the codebase (this correlates with MINOR in semantic versioning).

3.  `BREAKING CHANGE:` a commit that has a footer **_BREAKING CHANGE:_**, or appends a **_!_** after the type/scope, introduces a breaking API change (correlating with MAJOR in semantic versioning). A BREAKING CHANGE can be part of commits of any type.

4.  types other than `fix:` and `feat:` are allowed, for example @commitlint/config-conventional (based on the the Angular convention) recommends **_build:_**, **_chore:_**, **_ci:_**, **_docs:_**, **_style:_**, **_refactor:_**, **_perf:_**, **_test:_**, and others.

5.  footers other than `BREAKING CHANGE: <description>` may be provided and follow a convention similar to git trailer format.

        $ npm i git-commit-msg-linter // valida os commits, precisam ter um type na frente

        ************* Invalid Git Commit Message **************
        commit message: add commit linter
        correct format: <type>(<scope>): <subject>
        example: docs: update README add developer tips

        type:
          feat     A new feature
          fix      A bug fix
          docs     Documentation only changes
          style    Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
          refactor A code change that neither fixes a bug nor adds a feature
          test     Adding missing tests or correcting existing ones
          chore    Changes to the build process or auxiliary tools and libraries such as documentation generation
          perf     A code change that improves performance
          ci       Changes to your CI configuration files and scripts
          build    Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
          temp     Temporary commit that won't be included in your CHANGELOG

        scope:
          Optional, can be anything specifying the scope of the commit change.
          For example $location, $browser, $compile, $rootScope, ngHref, ngClick, ngView, etc.
          In App Development, scope can be a page, a module or a component.

        subject:
          Brief summary of the change in present tense. Not capitalized. No period at the end.

---
