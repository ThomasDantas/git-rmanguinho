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
