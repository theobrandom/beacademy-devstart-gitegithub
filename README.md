# Comandos básicos para uso do Git e GitHub

Para verificar a versão do git instalada utilize `git --version`.

Para listar os comandos do git utilize `git`.

Para fazer a configuração inicial no git, identificando quem está operando a ferramenta, utilizam-se os seguintes comandos:

```

git config --global user.name "Seu nome"
git config --global user.email "seuemail@servidordoemail.com"

```
> ***Obs.: A configuração inicial é muito importante para que o git possa registrar e associar o usuário durante cada etapa do versionamento do projeto.***

Para inicializar um repositório a partir do diretório de trabalho atual, criando conjuntamente uma ramificação principal, use `git init`.

Para inspecionar um repositório, verificando as informações do diretório, use `git status`.

Para adicionar um arquivo de alteração, visando atualização do diretório no próximo commit, use `git add <nomedoarquivo>`.

> ***Obs.: Não implica em efeito real no repositório, as alterações só serão gravadas, de fato, após o commit.***

> *Obs.2: No lugar do "<nomedoarquivo>" pode ser utilizado "." para representar uma quantidade X total de arquivos que estão na "espera" para ser adicionado.*

Para desfazer um git add, ou seja, retroceder a ação de adição de um arquivo que você fez no diretório, basta usar o comando `git rm --cached <nomedoarquivo>`.

Para guardar o estado do seu repositório naquele momento, ou seja, para fazer um commit, basta usar `git commit -m "Mensagem explicando o commit - Exemplo: Versão inicial"`.

Para mostrar um histórico das operações trabalhadas (commits) use `git log`.

Para gerenciamento de branchs (listar, criar, permutar, excluir e mesclar branchs, respectivamente), os comandos disponíveis são:

```

git branch
git branch nome_da_branch
git checkout -b nome_da_branch
git branch -d nome_da_branch
git merge nome_da_branch

```
> ***Obs.: Ao permutar de branch se atente para as pendências de commit, ou você deve finalizá-las realizando o git commit ou você precisa usar o `git stash` para arquivar as alterações na cópia do trabalho, para que assim você possa trabalhar em outra coisa e voltar e fazer a reaplicação mais tarde (opção muito útil na necessidade expressa de alteração de contexto e não se está pronto para um commit).***

> *Obs.2: A versão do comando checkout com o -b sinaliza uma criação de branch concomitante com permuta do ponteiro para essa branch, para uma permuta isolada, não usar o -b.*

> *Obs.3: Para realizar a mesclagem (git merge) é preciso estar na branch que se deseja manter as informações finais de mesclagem e apontar, no códio, o nome da branch que irá fornecer as informações para que essa mesclagm ocorra."
*Obs.3.1: Após a mesclagem de arquivos (git merge), é uma boa prática excluir a(s) branch(s) usada(s) durante a transição, já que esta(s) não será(ão) mais necessária(s).*

Para descartar as mudanças identificadas (ao invés de add) use `git restore <nomedoarquivo>`.

Para quaisquer dúvidas ainda restantes, com relação aos comandos do git, favor consultar a [documentação do git](https://git-scm.com/doc).

Para orientações sobre a Sintaxe básica de escrita e formatação no GitHub consultar [documentação](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

Para orientações sobre criação de chaves SSH (integração Git e GitHub) consultar este [tópico](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

Para iniciar um novo repositório no GitHub basta ir na parte dedicada aos repositorios na página, clicar em `new` e preencher as informações deste, sendo importante saber que o repositório pode ser público ou privado e que pode ou não já ser iniciado com uma branch main. Para que seja iniciado já constando uma branch main basta selecionar a opção `Add a README file`.

***Não é necessário selecionar a opção `Add .gitignore`, esta será responsável para designar uma lista de arquivos/diretórios que não serão acompanhados pelo controle de versão do Git.*** 

Para fazer o clone de um projeto remoto para a máquina basta ir até a opção `Code`, aba `SSH` (caso tenha configurado a nova chave SSH anteriormente) e copiar o código disponível. Em seguida, abra o terminal a partir do diretório local que deseja hospedar o clone e utilize o código `git clone` seguido na mesma linha do código anteriormente copiado. Automaticamente o clone será disponibilizado.

Para gerenciar o conjunto de repositórios remotos exibindo o endereço URL detalhado após o nome use `git remote -v`.

Para que as alterações do commit sejam identificadas na plataforma do GitHub é imprescindível que se use `git push` (essa etapa apresentará um erro caso a conexão com a chave SSH não tenha sido estabelecida corretamente).