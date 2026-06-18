# GitHub-Comandos
Todos os comandos que eu acho útil para se usar no terminal.

### git init
- Usado para criar um novo repositório em relação ao diretório.
### git clone "url"
- Você faz um clone do repositório original no Github dentro da sua máquina.
### git status
- Realiza uma busca e análise dos eu projeto atual, dizendo se as alterações do seu código podem ser commitadas ou não.
### git add
- Permite você adicionar as mudanças em relação ao repositório local, permitindo você conseguit dar commit.
- git add . permite você adicionar todos os arquivos de uma vez só.
### git commit -m "mensagem"
- git commit serve para registrar as mudanças no repositório local.
- -m "mensagem é para você atribuir o commit a um título. Organização.
### git log
- Mostrar o histórico dos commits ao longo do projeto.
### git push "nome_repositório" "branch"
- Para enviar a alteração do repositório.
### git pull "nome_repositório" "branch"
- Serve para atualizar o seu repositório local em relação ao repositório remoto se houve alguma alteração.
### git revert "id_commit"
- Ao usar o git log, cada commit tem um ID único. Basta usar ele e o git revert para reverter um commit.
### git reset --hard "id_commit"
- Serve para apagar o commit feito na máquina.
- Precisa usar o ID anterior, ou o ID que você queira voltar. Nunca aquele que você quer realmente apagar.
### git commit --ammend -m "mensagem"
- Serve para editar o título de um commit caso já enviado.
### .gitignore
- Para uma pasta ou arquivo não ser mostrado no github ao público, basta colocar os nomes da pasta o arquivo dentro do .gitignore.
### git diff --help
- Serve para comparar entre dois gits.
### git branch
- Mostra todas as ramificações do projeto.
- git branch -D "nome_branch" para deletar uma ramificação.
- git branch "nome_branch" para criar uma ramificação.
- git switch "nome_branch" para se locomover entre as ramificações.
### git merge "nome_branch"
- Serve para mesclar uma ramificação com a main.
### git rebase
- Serve para atualizar o código da ramificação em relação a main.
### git stash
- Serve para guardar uma modificação sem criar uma commit.
- git stash pop restaura a modificação guardada.
- git stash clear para limpar a lista de modificações guardadas.
- git stash push -m "mensagem" para atribuir uma nomenclatura específica para o stash.
### git restore
- Para desfazer alterações sem ter dado commit, voltando ao commit anterior.
