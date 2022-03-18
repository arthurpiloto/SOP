# SOP (Sistemas Operacionais)
* https://winworldpc.com/library/operating-systems

## Comandos (prompt de comando)
* dir ==> mostra pastas
* cls ==> limpa tela
* mkdir ==> cria pastas
* mkdir "nome composto" ==> Ex: mkdir "Sistema Operacional"
* rmdir ==> apaga ==> apaga pastas
* echo > ==> redirecionamento, apenas sobrescreve/substituí o conteúdo
* echo >> ==> redirecionamento, acrescenta conteúdo
* type ==> lê arquivos
* del ==> apaga arquivos
* attrib ==> exibe ou altera atributos
* start ==> abre programas desejados
* tree ==> mostra toda a "árvore" da pasta

### Comandos que exigem permissão de Administrador
* net user ==> usado para gerenciar e ver os usuários do computador
* net user (nome do usuário) /add ==> cria um usuário
* net user (nome do usuário) (senha) /add ==> cria uma senha para o usuário
* net user (nome do usuário) /fullname:"" ==> coloque o nome completo do usuário selecionado

Você é capaz de juntar todos os comandos em um só:
    
    net user pedro Senai@127 /add /fullname:"Pedro da Silva"

* net user (nome do usuário) "*" ==> trocar a senha de usuário
* net localgroup administradores (nome do usuário) /add ==> adicionar um usuário como Administrador
* net localgroup administradores (nome do usuário) /delete ==> deleta um usuário como Administrador

## Linux (curso na Cisco)
* As habilidades do Linux são necessárias para muitas faixas profissionais de TI. Por exemplo, o conhecimento de comandos básicos do Linux é um pré-requisito para programas de certificação de TI

### Comandos
Os comandos são sensitive case, ou seja, há distinção entre letras maiúsculas e minúsculas.

* O comando ``` ls ```  exibe uma lista de informações sobre arquivos.

A maioria dos comandos segue um padrão simples de sintaxe:

``` comando [opcoes…] [argumentos…] ```

Em outras palavras, você digita um comando, seguido de quaisquer opções e/ou argumentos antes de pressionar a tecla Enter. Normalmente, as opções alteram o comportamento do comando e os argumentos são itens ou valores para o comando agir.

O comando ``` pwd ``` pode ser usado para mostras sua localização atual dentro de um sistema de arquivos.

O comando ``` ls ``` é usado para listar o conteúdo de um diretório.

### Argumentos
Um argumento pode ser usado para especificar algo para o comando agir. O comando ``` ls ``` pode ser dado o nome de um diretório como um argumento, e ele irá listar o conteúdo desse diretório.

Como o Linux é de código aberto, existem alguns segredos interessantes que foram adicionados pelos desenvolvedores, pesquise-os para saber mais!

### Opções
As opções podem ser usadas para alterar o comportamento de um comando. O comando ``` ls ``` foi usado para listar o conteúdo de um diretório e a opção ``` -l ``` resulta em uma saída de "exibição longa", ou seja, fornece mais irformações sobre cada um dos arquivos listados.

Muitas vezes, o caractere é escolhido para ser mnemônico para o seu propósito, como escolher a letra "l" para longo ou "r" para reverso. Por padrão o comando ``` ls ``` imprime os resultados em ordem alfabética, se adicionarmos a opção ``` -r ``` irá imprimir os resultados em ordem alfabética inversa.

As opções podem ser usadas de uma só vez, por exemplo ``` ls -l -r ``` ou ``` ls -rl ``` ou ``` ls -lr ```. Todas as opções vão gerar o mesmo resultado.

### Diretórios
Os diretórios são um tipo de arquivo usado para armazenar outros arquivos, eles fornecem uma estrutura organizacional hierárquica.

<img alt="Hierarquia de pastas e arquivos" src="./img-README/diretorios.png">

Use o comando ``` cd ``` para navegar e alterar entre diretórios.

``` cd [opcoes…] [argumentos…] ```

Os diretórios são equivalentes a pastas no Windows e Mac OS. Assim como esses sistemas operacionais mais populares, uma estrutura de diretórios Linux tem um nível superior. Não é chamado de “Meu Computador”, mas sim o diretório root (raiz) e é representado pelo caractere "/". Para mover para o diretório root, use o caractere "/" como argumento para o comando ``` cd ```.

O argumento para o comando ``` cd ``` é mais do que apenas o nome de um diretório, na verdade é um caminho. Um caminho é uma lista de diretórios separados pelo caractere "/".

---
Se você pensar no sistema de arquivos como um mapa, os caminhos são as direções passo a passo; eles podem ser usados para indicar a localização de qualquer arquivo dentro do sistema de arquivos. Existem dois tipos de caminhos: absoluto e relativo. Os caminhos absolutos começam na root do sistema de arquivos, os caminhos relativos começam a partir da sua localização atual.

* Caminho absoluto: Um caminho absoluto permite que você especifique a localização exata de um diretório.
* Caminho relativo: um caminho relativo fornece direções para um arquivo relativo à sua localização atual no sistema de arquivos. Os caminhos relativos não começam com o caractere "/", eles começam com o nome de um diretório.
---

#### Atalhos
* Os caracteres "..": Independentemente do diretório em que você esteja, os caracteres ".." sempre representa um diretório maior em relação ao diretório atual, às vezes referido como o diretório pai. Mais resumidamente, os caracteres ".." são usados para voltar um diretório.
* O caractere ".": Independentemente do diretório em que você esteja, o caractere . sempre representa seu diretório atual. Para o ``` cd ``` este atalho não é muito útil, mas será útil para comandos cobertos nas seções subsequentes.
* O caractere "~": Usado para retornar ao seu diretório home a qualquer momento, execute o seguinte comando: ``` cd ~ ```.

### Acesso Administrativo
Existem muitos comandos Linux que lidam com informações confidenciais, como senhas, hardware do sistema, ou de outra forma operam sob outras circunstâncias excepcionais. Impedir que usuários regulares executem esses comandos ajuda a proteger o sistema. Fazer login como usuário root fornece acesso administrativo, permitindo a execução de alguns dos comandos privilegiados.

#### O comando ``` su ```

``` su [opções] [nome-do-usuário] ```

O comando ``` su ``` permite que você atue temporariamente como um usuário administrador. Ele faz isso criando um novo console de entrada de texto que permite digitar comandos, chamado shell. Para sair e retornar à conta, use o comando ``` exit ```.

Depois de executar o comando, uma senha é necessária. Você consegue mudar ou definir a senha de algum usuário escrevendo o comando ``` password [nome-do-usuário] ```.

<img alt="Painel de controle" src="./img-README/painel-su.png">

#### O comando ``` sudo ```

``` sudo [opções] [comando] ```

O comando ``` sudo ``` permite que você execute um comando como usuário administrador sem criar um novo shell. O comando ``` sudo ``` também pode ser usado para alternar para outras contas de usuário. Para especificar uma conta de usuário diferente, use a opção ``` -u ```.

Assim como o comando ``` su ```, o ``` sudo ``` também pede senha para entrar no usuário.

Execute o comando ``` sl ``` como usuário root colocando ``` sudo ``` na frente dele.

<img alt="Painel de controle" src="./img-README/painel-sudo.png">

### Permissões 
As permissões determinam as maneiras pelas quais diferentes usuários podem interagir com um arquivo ou diretório.

Vamos usar as informações de um arquivo exemplo para mostrar as informações necessárias:

    -rw-r--r-- 1 sysadmin sysadmin 647 Dec 20  2017 hello.sh

<img alt="Campos relevantes para permissões" src="./img-README/permissoes.png">

#### Tipos de permissão
Existem três permissões diferentes que podem ser colocadas em um arquivo ou diretório: ler, gravar e executar. A maneira pela qual essas permissões se aplicam difere para arquivos e diretórios.

<img alt="Tabela de tipos de permissões" src="./img-README/tabel-permissoes.png">

#### Alterando Permissões
O comando ``` chmod ``` é usado para alterar as permissões de um arquivo ou diretório. Somente o usuário administrador (root) ou o usuário que possui o arquivo é capaz de alterar as permissões de um arquivo. Existem duas técnicas para alterar as permissões: Simbólico e Octal. O método simbólico é bom para alterar um conjunto de permissões de cada vez. O método octal ou numérico requer o conhecimento do valor octal de cada uma das permissões e requer que todos os três conjuntos de permissões (usuário, grupo, outros) sejam especificados a cada vez.

Por uma questão de simplicidade, apenas o método simbólico será coberto.
    
    chmod [<conjunto><ação><permissões>]... arquivo
    
Para usar o método simbólico de ``` chmod ``` você deve, primeiro, indicar qual conjunto de permissões está sendo alterado.

<img alt="Tabela com o conjunto de permissões" src="./img-README/conjunto-permi.png">