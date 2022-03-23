# git


## Comandos iniciais
|Comando|Descrição |
|-------|----------|
|`git version`|Ver versão|
|`git config --global user.name “seu_user”`|Adicionar usuário|
|`git config --global user.email “seu_email@email.com”`|Adicionar e-mail|
|`git config --global core.editor “caminho do executável do editor: Ex: C:\Users..”`|Adicionar/alterar editor|
|`git config user.name`|Ver usuário|
|`git config user.email`|Ver e-mail|
|`git config core.editor`|Ver editor|


## Comandos básicos do dia a dia

Quando trabalhamos em um projeto com várias pessoas, recomenda-se utilizar branches para fazer alterações antes de publicar na `master`/`main`.

|Comando|Descrição |
|-------|----------|
|`git pull`|Puxar os novos arquivos (importante fazer isso TODA vez que for mexer no projeto)|
|`git checkout -b <nome_branch>`|Altera a branch|
|`git add .`|Prepara todos (.) os arquivos para serem comitados|
|`git commit -m "<message>"`|Commita todos os arquivos preparados para serem comitados. O commit terá o nome `<message>`. |
|`git push`|Sincroniza as alterações com o repositório remoto pela primeira vez|
|`git push --set-upstream origin <nome_branch>`|Sincroniza as alterações com o repositório remoto|

### Passo a passo
Depois de setar todo o git na máquina, além de clonar o repositório, para sintetizar os comandos acima, está descrito a seguir:

Ao clonar o repositório, você estará na branch principal (`master` ou `main`). Ai sempre você coloca:
`git pull` = pra atualizar os arquivos `main`.
Quando você trabalha em time ou está num projeto grande, é recomendado criar uma branch pra fazer as alterações. Pra criar a branch:
`git checkout -b <nome_branch>` = cria branch nova

Após alterar os arquivos, deve-se  e pra colocar do git pro github:
`git add .` = prepara todos `(.)` os arquivos para serem comitados OU
`git add <nome_arquivo>` = preparar cada arquivo
`git commit -m "<message>"` = commita todos os arquivos preparados para serem comitados. O commit terá o nome `<message>`. 
`git push` -> pra subir os arquivos

Então você pode abrir um Pull Request (PR).

Pra voltar pra master:
`git checkout <nome_branch>` = entrar/trocar de branch
E executar dar um `git pull` novamente.


## Outros comandos 
|Comando|Descrição |
|-------|----------|
|`git clone <ulr>`[^clone]|clona o repositório para seu computador local|
|`git branch`|verifica quais branches locais existem no seu computador|
|`git branch -a`|lista todas as branches (locais e remota)|
|`git branch -d <nome_branch>`|remove a branch|
|`git branch -D <nome_branch>`|apaga mesmo que não tenha mergeado|
|`<git rm -r <arquivo_ou_repositorio>`||
|`git status`|ver se há uma modificação|
|`git mv <nome_pasta_antiga> <nome_pasta_nova>`|Renomear arquivos e pastas (problema que atualiza o commit de todos os arquivos)|
|`git mv nomeArquivo nome_pasta`|Alterar arquivo de pasta|
|`git diff .`|Ver as alterações de todos os arquivos|
|`git checkout -- .`|Apaga todas `(.)` as alterações não commitadas|
|`git reset HEAD~1`|Reverte alterações commitadas (último commit)|
|`git commit --amend -m "Nova mensagem de commit"`|Mensagem de commit errada|
|`git commit -m "Empty Commit" --allow-empty`|Commit vazio|
|``||
|``||
|``||
|``||
|``||
|``||



### Template tabela
|Comando|Descrição |
|-------|----------|
|``||
|``||
|``||
|``||
|``||
|``||
|``||
|``||
|``||

[^clone]: ir no repositório do github de interesse > code > copiar link
