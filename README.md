# GitHub-Comandos
Aqui foi feito uma planilha sobre os estudos de git/github com a nomenclatura de cada comando essencial do git, ela não só vai te dar uma lista mas também vai lhe guiar ao decorrer do trabalho.

## Start
Começamos entre dois comandos: um para criar um repositório local do zero ou clonar um repertório remoto no GitHub.
### git init
- Criar repertório;
### git clone <url>
- Clonar repertório;
----
Caso for um repertório criado na sua máquina, precisa conectar o repertório local ao remoto(GitHub) através de um único comando.
### git remote add <nome> <endereço_remote>
- Normalmente nomeamos o repertório como origin, não algo obrigatório mas é uma boa prática;
- O endereço_remote é a URL do repositório on-line no qual você queira conectar;
## Controlando as versões
Agora que iniciamos o nosso projeto teremos alterações e iremos precisar salva-lás, organizar elas também. Mas primeiro vamos aprender a organizar elas através das boas práticas antes de tudo.
Primeiro vamos criar uma ramificação já que alterar os dados diretamente da main é perigoso, com o risco de não poder ou aumentar a dificuldade para desfazer a modificação.
### git branch
- Ele mostra todas as ramificações criadas no repertório;
- git branch <nome_branch> você cria uma ramificação própria;
- git switch <nome_branch> permite se locomover entre as ramificações;
- git branch -D "nome_branch" para deletar uma ramificação;
----
Ao concluir a função criada na branch, é hora de mesclar ela a main. Porém é preciso atualizar o repertório do que já foi feito que é a sessão dos commits.
### git status
- O git status vai realizar uma busca-análise do projeto, procurando pelos arquivos alterados que não foram postos no palco;
### git add <nome_arquivo> (ou) .
- O git add tem uso de encaminhar as alterações para o palco, o que vai permitir o uso do commit;
- <nome_arquivo> para adicionar algum arquivo modificad específico;
- . para adicionar todos os arquivos modificados;
### git commit -m "mensagem"
- O commit finalmente vai registrar as mudanças feitas no repositório local;
- O commit vem com um ID único;
- Caso erro na mensagem é usado o git commit --ammend -m "mensagem" para alterar o ÚLTIMO commit;


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
### .gitignore
- Para uma pasta ou arquivo não ser mostrado no github ao público, basta colocar os nomes da pasta o arquivo dentro do .gitignore.
### git diff --help
- Serve para comparar entre duas commits.
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
### git tag "nome"
- Cria um checkpoint, uma versão no projeto.
- git push "nome_repositório" "tag" para enviar a tag para o repertório remoto.
- git push "nome_repositório" --tags para mandar todas as tags
- git tag -a "nome" -m "mensagem"
