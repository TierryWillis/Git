<h1 align="center"> Git </h1>

## Comandos Git (atalhos)

Nome
```
$ git config --global user.name "Fulano de Tal"
```

E-mail
```
$ git config --global user.email fulanodetal@exemplo.br
```

Criar diretório
```
mkdir nome-diretorio
```

Criar arquivo na pasta
```
touch nome-diretorio/nome-do-arquivo.md
```

Entrar no diretório
```
cd nome-diretorio
```

Transformar no repositório Git
```
git init
```

Clona o repositório remoto
```
git clone código https do repositório remoto NOME
```

Criar um README vazio
```
touch README.md
```

Verificar Status
```
git status
```

Adicionar modificações
```
git add .
```

Criar Commit
```
git commit -m"frase commit"
```

Verificar os Commits
```
git log
```

Conectar o Repositório local ao Remoto
```
git remote add origin código https do repositório remoto
```

Enviar alterações para o repositório Remoto
```
git push -u origin main
```

Receber as atualizações do repositório Remoto no repositório Local
```
git pull
```


## Como usar o Git

- **Configure seu nome de usuário e e-mail:** 
O Git registra quem fez cada alteração no código. Use os comandos, no terminal:
```
git config --global user.name "Your name"
```

- **Criação do Repositório Git:**
Para começar a rastrear seu código, crie um repositório Git em seu projeto. Navegue até a pasta do seu projeto e digite:
```
git init
```

- **Adicionar Arquivos ao Controle da versão**
Utilize o comando ```git add ``` para adicionar arquivos no local em que são preparados e "commitados" ou salvos.
```
git add nome-do-arquivo
```

- **Commite**
Um commit é um snapshot de suas alterações. Use o comando ```git commit``` para criar um commit com uma mensagem descritiva do que foi alterado no projeto.
```
git commit -m "Sua mensagem de commit"
```

- **Visualização do histórico de Commits**
Use ```git log``` para ver o histórico de commits no repositório.


### Principais comandos do Git
- **Git Init**
O comando ```git init``` é utilizado para iniciar um repositório Git em um diretório no sistema. Após a execução deste comando, a ferramenta começa a monitorar o estado dos arquivos no projeto.

- **Git Clone**
O comando ```git clone``` é utilizado para copiar um repositório remoto para um diretório local na máquina. Este repositório pode ser criado a partir de um repositório armazenado localmente, utilizando o caminho absoluto ou relativo, ou pode ser remoto, utilizando o URI na rede.
**Com um repositório clonado, é possível acompanhar o progresso de um projeto e suas modificações, além de contribuir para o projeto enviando suas mudanças para o repositório central.**

- **Git Status**
O comando ```git status``` é utilizado para verificar o estado de um repositório Git, bem como o status do repositório central. Ele mostra informações sobre se o projeto local está sincronizado com o repositório central, quais arquivos estão sendo monitorados pelo Git e em qual branch você está no projeto.

- **Git Add**
O comando ```git add``` é utilizado para adicionar arquivos ao conjunto de alterações a serem feitas. É possível adicionar um único arquivo, múltiplos arquivos de uma vez, como git add ```<arquivo1> <arquivo2> ...```, ou até mesmo um diretório inteiro através de seu caminho. Uma vez que um arquivo é adicionado ao conjunto de alterações com o comando ```git add```, ele está pronto para ser incluído no próximo **commit**.

- **Git Branch**
O comando ```git branch``` é utilizado para criar novos ramos de desenvolvimento, bem como visualizar quais são os ramos existentes.
Para criar um novo ramo, basta usar o comando ```git branch``` seguido do nome do novo ramo. Para visualizar os ramos existentes, basta não informar um nome para a nova branch, e todas as já criadas serão listadas.

- **Git Checkout**
O comando ```git checkout``` é utilizado para navegar entre as versões do projeto, bem como entre as diferentes ramificações criadas. Para navegar entre as versões, basta usar o comando:
```
git checkout <hashcode do commit>
```
E todo o estado do projeto será modificado para o estado no qual o commit foi feito. Similarmente, para navegar entre as ramificações podemos usar o comando:
```
git checkout <nome da branch>
```
E a branch será alterada. O comando também permite criar uma branch e imediatamente mudar para ela, através do comando:
```
git checkout -b <nome da branch>
```

- **Git Diff**
O comando ```git diff``` é utilizado para visualizar modificações feitas entre commits, sejam eles entre um commit arbitrário e o estado atual do projeto, dois commits arbitrários, ou até mesmo todas as alterações entre dois commits distintos.
Para visualizar as alterações entre um commit distinto e o atual, basta usar o comando:
```
git diff <hashcode do commit anterior>
```

- **Git Config**
O comando ```git config``` é usado para configurar e personalizar o ambiente Git no seu sistema. Ele permite que você defina informações como seu nome de usuário, endereço de e-mail, editor padrão e muitas outras configurações que definem como o Git interage com seus repositórios.
A estrutura básica do comando é:
```
git config <opções> chave valor
```
```<opções>```: Pode ser global **(--global)** para definir configurações para todos os repositórios no seu sistema ou local **(--local)** para definir configurações específicas para um repositório em particular.

```chave```: A chave de configuração que você deseja definir (por exemplo, user.name para o nome de usuário).

```valor```: O valor que você deseja atribuir à chave (por exemplo, seu nome de usuário ou endereço de e-mail).

### União dos Repositórios Remotos e Locais
**Iniciar um Repositório Git Local:** Caso seu projeto ainda não seja um repositório Git, utilize o comando ```git init``` para iniciá-lo.

**Adicionar o Remote:** Use o comando ```git remote add origin <URL-do-Repositório>``` para adicionar o repositório remoto como um **"remote"** denominado **"origin"**.
```
git remote add origin https://github.com/seu-usuario/seu-repositorio.git
```

### Enviando os Commits para o Repositório Remoto

Criar um Arquivo **README (Opcional):** Se ainda não tiver um arquivo **README** que explique o projeto, suas funcionalidades, pré-requisitos etc. Para criar o arquivo, utilize o seguinte comando:
```
echo "# Meu Projeto" >> README.md
```
- **Adicionar e Fazer o Commit:** 
No terminal, utilize os comandos ```git add``` e ```git commit``` para adicionar e confirmar as alterações.
```
git add README.md
git commit -m "Adicionando arquivo README"
```

- **Definir o Nome da Branch Principal:** 
Se estiver utilizando a versão mais recente do Git, a branch principal é chamada "main". Utilize o comando ```git branch -M main``` para definir isso.
```
git branch -M main
```

- **Enviar para o Repositório Remoto:** 
Utilize o comando ```git push -u origin main``` para enviar os commits para o repositório remoto.
```
git push -u origin main
```

### Baixar novos Commits do Repositório Remoto
- **Navegue até o diretório do repositorio local:**
```
cd <caminho/do/seu/repositorio>
```

- **Atualize o Repositório Local com os Novos Commits:** 
Use o comando ```git pull``` para obter os novos commits do repositório remoto e atualizar sua **branch** local.
```
git pull origin nome-da-branch
or
git pull origin main
```

### Tratamento de Conflitos
- **Verifique as Alterações Locais:** 
Após o ```git pull```, você pode verificar as alterações locais usando ```git log``` para visualizar os novos commits no histórico do seu repositório.
```
git log
```

### Branches
**As branches podem ser usadas para isolar o desenvolvimento de diferentes funcionalidades. Cada branch representa uma linha independente de desenvolvimento. Por exemplo, você pode ter uma branch para desenvolver uma nova funcionalidade, outra para corrigir um bug, e assim por diante.**
```
git branch nome-branch
```

Para mudar para a nova branch:
```
git checkout nova-funcionalidade
```

- **Branches de Funcionalidades:**
É comum usar branches específicas para cada funcionalidade que está sendo desenvolvida. Isso mantém as alterações relacionadas a uma funcionalidade isoladas de outras partes do código.
```
git checkout -b feature/nova-função
```

- **Git Merge**
Após completar o desenvolvimento em uma branch de funcionalidade, você pode mesclar as alterações de volta para a branch principal (por exemplo, **"main"** ou **"master"**). Isso integra a nova funcionalidade ao código principal.
Para mudar para a branch principal:
```
git checkout main
```
Em seguida, mescle as alterações da feature de volta para a branch principal:
```
git merge feature/nova-funcionalidade
```


## Referências
[DIO](https://www.dio.me/articles/lista-dos-principais-comandos-do-git)

[Alura](https://www.alura.com.br/artigos/o-que-e-git-github)



