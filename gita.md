# Gita

Gita é uma solução open-source desenvolvida por [nosarthur](https://github.com/nosarthur/) para mexer em vários repositórios do github ao mesmo tempo.

## Instalação
Instalar gita: https://github.com/nosarthur/gita 

## Comandos
Entrar no diretório onde estão os repositórios do git.

Para ver todos os repositórios detalhados
`ll`

Para adicionar os repositórios no contexto gita:
`gita add repo1 repo2`

Para atualizar todos os repositórios de uma vez:
`gita pull`

Para verificar os repositórios:
`gita ll`

Para adicionar grupos:
`gita group add -n group-name repo1 repo2`

Verificar grupos:
`gita group`

Para ver o status:
`gita st group-name`

Para remover arquivo:
`gita shell group-name rm -rf file_name`

Para criar arquivo:
`gita shell neurons mkdir .github/workflows`

## Exemplo como copiar arquivos de um repositório para outros:
```
gita super neurons checkout master
gita super neurons pull
gita super neurons checkout -b pde-4023
gita shell neurons rm -rf .circleci
gita shell neurons mkdir .github/workflows
yes | gita shell neurons cp -rf ~/Documents/git/neuron-example/.github/ .
gita super neurons add .
gita super neurons commit -m "[PDE-4023] CI: Add GHA workflows"
gita super neurons git push --set-upstream origin pde-4023
```


