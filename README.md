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
### git remote add <nome <endereço_remote>
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
- Ele mostra o histórico de commits e seus IDs;
----
As vezes nós erramos ao fazer um commit, seja esquecer de algum código ou enviar o commit sem querer. Mas está tudo bem, para isso temos duas opções.
### git revert <ID_commit>
- Esse comando reverte o commit feito, criando um commit em cima dele com a versão passada;
### git reset --hard <ID_commit>
- Esse comando você apaga o commit. É a forma mais radical de voltar para trás;
- Para usar esse comando, é necessário pegar o commit anterior da atual para apgar;
### git restore
- Desfaz as alterações já adicionads mas ainda não commitadas;
### git pull --rebase
- Pode ser que outra pessoa esteja trabalhando na mesma branch que a sua, isso gera um conflito onde a máquina precisa colocar duas commits no mesmo lugar. Com o comando acima é resolvido por deixar a sua commit acima a da outra pessoa;
- Caso não funcione pois as duas commits estejam dando erro, use o git pull --rebase abort para desfazer o pull rebase;
- E então com o conflito e ter que usar o abort, é preciso usar o git pull;
----
E outras vezes queremos organizar o nosso trabalho, ou deixar para depois. Até mesmo deixar invisível alguns arquivos mais sensíveis do projeto;
### .gitignore
- Você cria ele como uma pasta dentro do diretório, e tudo que colocar nele vai ficar invisível no github para o público geral;
### git diff
- git diff <commit_1> <commit_2> tem o uso para comparar entre dois commits distintos;
- git diff --staged tem o uso para comparar alterações já adicionadas;
- git diff --cached tem o uso de mostrar as alterações que você já fez;
### git stash
- Você não consegue trabalhar em outra branch se não tiver feito o commit do arquivo alterado normalmente, mas com o git stash você pode guardar as alterações numa gaveta para depois;
- git stash pop vairestaurar a modificação guardada;
- git stash clear vai limpar a lista de modificações guardadas;
- git stash push -m "mensagem" faz que ao invés de só guardar a alteração, você dê a ela um nome;
# Finish
E então chegamos ao fim deste guia, onde também significa o fim de um ciclo do projeto seja ele completamente feito ou apenas uma atualização pronta para ser lançada.
### git push <repertório_nome> <branch>
- Você pega o commit que fez que envia diretamento para o repositório remoto;
### git merge <branch_nome>
- Com esse comando você mescla duas ramificações, comumente a main com uma outra que tenha as atualizações para o projeto;
### git rebase
- Ao invés de mesclar, criando uma nova commit que junta as duas branchs. O git rebase é a versão gourmet onde ao invés de mesclar ela move a ramificação dentro da main como uma continuação;
- Esse comando tem a prática de deixar o histórico de commits mais limpo, muito utilizado pelas empresas. Outra dica é tomar cuidado com o git pull, ela pode acabar com o padrão da empresa(Verificar com o seu chefe qual padrão a empresa usa.);
----
# git tag <nome>
- Ele é usado para o pré-lançamento de uma versão, usando uma commit como referência, um checkpoint;
- git push <nome_repositório> <tag> para enviar a tag para o repertório remoto;
- git push "nome_repositório" --tags para mandar todas as tags;
- git tag -a <nome> -m <mensagem> para adicionar o nome da tag e uma mensagem explicando o que a versão é;

Muito obrigado por ler até o final!
Créditos: Gabriel Del Sole Speck
