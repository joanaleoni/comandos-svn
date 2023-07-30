# Comandos SVN (Subversion)

<img align='center' src='https://subversion.apache.org/images/svn-name-banner.svg' width='900'>

## Comandos básicos
`svnadmin create </caminho/para/repo>`  
Cria um novo repositório SVN no caminho especificado  

`svn info`  
Exibe as informações do repositório .svn  

`svn checkout <url-do-repositorio-origem> <caminho-do-diretorio-destino>`  
Gera uma cópia de trabalho do repositório  

`svn update`  
Atualiza a cópia de trabalho com as alterações do repositório central   

`svn status`  
Exibe o status de arquivos e diretórios  

`svn diff`  
Exibe as diferenças entre a cópia de trabalho e o repositório SVN central  

`svn log`  
Exibe o histórico de revisões do repositório  

## Commitando alterações
`svn add <arquivo-ou-diretorio>`  
Adiciona um arquivo ou diretório para versionamento  

`svn commit -m 'mensagem explicativa das alterações realizadas'`  
Envia as alterações para o repositório SVN central  

## Edição de propriedades
`svn propset <nome-da-propriedade> <valor-da-propriedade> <alvo>`  
Define uma propriedade  

`svn proplist <alvo>`  
Lista todas as propriedades definidas no arquivo ou diretório especificado  

`svn propget <nome-da-propriedade> <alvo>`  
Exibe o valor de uma propriedade específica associada ao arquivo ou diretório  

`svn propdel <nome-da-propriedade> <alvo>`  
Exclui a propriedade do arquivo ou diretório  

`svn propedit <nome-da-propriedade> <alvo>`  
Edita o valor de uma propriedade através de um editor externo  

## Ignorando arquivos
`svn propset svn:ignore <padrao> <diretorio>`  
Ignora arquivos ou diretórios que contêm o padrão especificado  

`svn propget svn:ignore .`  
Exibe a lista de padrões de arquivos e diretórios que estão sendo ignorados  

## Revertendo alterações
`svn revert <arquivo>`  
Reverte mudanças locais no arquivo especificado  

`svn revert -R <diretório>`  
Reverte mudanças recursivamente em todos os arquivos dentro do diretório especificado  

`svn merge -c -<número-da-revisao> <url-do-repositorio>`  
Desfaz um commit

## Branches
`svn copy <url-do-repositorio>/trunk <url-da-branch> -m "Criando uma branch"`  
Cria uma branch  

`svn list <url-do-repositorio>`  
Lista as branches já existentes  

`svn merge <url-da-branch>`  
Mescla a branch ao trunk (branch principal)  
