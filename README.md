# Github
Repositório para treinamento do git
<b>O básico sobre o Git</b><br />O básico para trabalhar em equipe com o Github<br />


## Conteúdo<a name="indice"></a>
1. [Básico](#basico)
    1. [Git Clone](#clone)
    2. [Git Pull](#pull)
    3. [Git Status](#status)
    4. [Git Add](#add)    
    5. [Git Commit](#commit)    
    6. [Git Push](#push)        
2. [Outros comandos](#outros)
    1. [Git RM](#rm)
    2. [Git Log](#log)
    3. [Git Shortlog](#shortlog)
    4. [Git Reflog](#reflog)    
    5. [Git MV](#mv)    
3. [Branch](#branch)
    1. [Modificar - Checkout](#modificarbranch)
    2. [Merge](#merge)    
4. [Stash](#stash)
    1. [Git Ignore](#ignore)
5. [Deu ruim](#caminhofeliz)


## BÁSICO <a name="basico"></a>
<a name="clone"></a>
<b>GIT CLONE</b><br/>
<b>git clone</b> passando a referência do repositório remoto. Utilize o comando quando for obter um novo projeto já criado e que não tenha baixado para seu computador. <br />
``` 
git clone https://github.com/alveselton/Alveselton.git
```

<a name="pull"></a>
<b>GIT PULL</b><br/>
<b>git pull</b> serve para recebermos atualizações do respositório remoto.<br />
``` 
git commit -a -m 'mensagem para identificar o motivo do commit'
```

<h3>Opa!! Editou o código ou o conteúdo e tem uma nova informação???<br />Uau! Então vamos subir para produção!</h3><br />

<a name="status"></a>
<b>GIT STATUS</b><br/>
git status exibe os arquivos que foram modificados/criados por você e que estão prontos para subir para o versionamento.<br />
``` 
git status 
```

<a name="add"></a>
<b>GIT ADD</b><br/>
git add esse é o cara que adicionará o arquivo ou os arquivos ao índice e irá preparar o conteúdo para o próximo commit.
Ops... falei COMMIT? Calma, ele será o próximo que irei comentar =)<br />
Observação: O "." (ponto sem aspas) quer dizer que você irá adicionar todos os arquvos modificados/criados ao índice.<br/>

``` 
git add . 
```

<a name="commit"></a>
<b>GIT COMMIT</b><br/>
git commit permite você grave suas alterações mais recentes no repositório.<br />Não quer perder seu dia de trabalho??? Faça um commit =)<br />
``` 
git commit -a -m 'mensagem para identificar o motivo do commit'
```

<a name="push"></a>
<br /><b>GIT PUSH</b><br/>
git push envia as alterações para o repositório remoto<br />É isso ai. Acabamos de enviar todo nosso trabalho e nossos colegas poderão atualizar o projeto em suas máquinas.
``` 
git push -u origin nome_branch
```

## OUTROS COMANDOS <a name="outros"></a>
<a name="rm"></a>
<b>GIT RM</b><br/>
git rm remove o arquivo.

``` 
git rm arquivo.txt
```

<a name="log"></a>
<br /><b>GIT LOG</b><br/>
git log exibe todas as informações dos commits realizados feitas no projeto. Matenha boas informações nas mensagens para um bom entendimento do que aconteceu no projeto.

``` 
git log
```

<a name="shortlog"></a>
<br /><b>GIT SHORTLOG</b><br/>
git shortlog exibe o log resumido do projeto. O commit será agregado por autor.

``` 
git shortlog
```

<a name="reflog"></a>
<br /><b>GIT REFLOG</b><br/>
git reflog exibe um log mais completo e exibe tudo o que aconteceu. Por padrão, o log é salvo por 30 dias.

``` 
git reflog
```

<a name="mv"></a>
<br /><b>GIT MV</b><br/>
git mv move ou renomeia sem perder a referência do arquivo. Para a origem é necessário o nome do arquivo e a extensão e para o destino é necessário a pasta, nome do arquivo e extensão.
<br />
Exemplo Mover

``` 
git mv nome-arquivo.txt folder/nome-arquivo.txt
```

Exemplo Renomear
``` 
git mv folder/nome-arquivo.txt folder/nome-arquivo-doc.txt
```

<a name="ignore"></a>
<br /><b>GIT IGNORE</b><br/>
git ignore serve para que determinados arquivos ou pastas não sejam enviados para o repositório. Útil para não versionar pastas de seguranças em repositório público, por exemplo.<br />
Estrutura de um arquivo .gitignore

``` 
nome-arquivo.txt
node_modules/*
```

<br /><b>Observação: Após alterar, incluir ou excluir qualquer arquivo é necessário commit e push para que o projeto seja atualizado no repositório.</b>


## BRANCH <a name="branch"></a>
<p>É a ramificação das versões do projeto. Diversas ramificações poderão ser criadas para o desenvolvimento do projeto. Por padrão utiliza-se o nome master ou main para identificar a branch de produção, porém podemos ter outras versões como desenvolvimento e homologação.</p>

<br /><b>GIT BRANCH</b><br/>
<b>git branch</b> lista todas as branchs disponíveis no projeto ou <b>git branch nome-branch</b> para criar uma nova branch.

``` 
git branch
```

Ou <br />


``` 
git branch nome-branch
```

<a name="deletarbranch"></a>
<br /><b>DELETANDO UMA BRANCH</b><br/>
<b>git branch -d</b> exclui o branch específico.

``` 
git branch -d nome-branch-deletada
```

<a name="modificarbranch"></a>
<br /><b>MUDANDO DE BRANCH</b><br/>
<b>git checkout nome-branch</b> seleciona uma branch específica para que possa ser modificada ou até que seja criada uma nova branch a partir dela.

``` 
git checkout nome-branch
```

<a name="merge"></a>
<br /><b>MERGE - HORA DE UNIR AS BRANCHES</b><br/>
<b>git merge nome-branch</b> será utilizando quando for necessário unir duas branches.<br />
1.) Selecione sua branch principal através do comando git checkout<br />
2.) Informe quando com branch você precisa fazer o merge 
``` 
git merge nome-branch
```

## STASH <a name="stash"></a>
<b>git stash</b> é utilizado para recomeçar o trabalho porque o resultado não era o esperado com aquele código e precisa salvar as alterações em algum local que possa recupera depois.<br />
1.) Para criar o stash
``` 
git stash
```

2.) Para listar o stash
``` 
git stash list
```

3.) Para utilizar o stash, sendo o 0 o número do indice do Stach
``` 
git stash apply 0 
```

4.) Para excluir o stash
``` 
git stash drop 0 
```

## ACABOU O CAMINHO FELIZ<a name="caminhofeliz"></a>
<h4>Sessão DEU RUIM</h4>

<br /><b>GIT CHECKOUT</b><br/>
git checkout ele volta para o estado original antes das alterações. Ele removerá "todas as mudanças" deixando igual a master.

``` 
git checkout nome-arquivo.txt
```

ou para mudar e criar uma nova branch use a flag -b<br />

``` 
git checkout -b nome-arquivo.txt
```

<br /><b>GIT RESET</b><br/>
git reset quando aplicado, ele irá resetar todas as mudanças de uma branch. Tanto os commits quanto as alterações pendentes serão excluídas. <br />
Portanto, identificou que será necessário voltar todo o código para uma versão anterior, sem a necessidade de salvar o código atual ?! 

``` 
git reset --hard origin/master
```
