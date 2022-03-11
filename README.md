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

## Linux (curso na Cisco)
* As habilidades do Linux são necessárias para muitas faixas profissionais de TI. Por exemplo, o conhecimento de comandos básicos do Linux é um pré-requisito para programas de certificação de TI

### Comandos
Os comandos são sensitive case, ou seja, há distinção entre letras maiúsculas e minúsculas.

* O comando ``` ls ```  exibe uma lista de informações sobre arquivos.

A maioria dos comandos segue um padrão simples de sintaxe:

``` comando [opcoes…] [argumentos…] ```

Em outras palavras, você digita um comando, seguido de quaisquer opções e/ou argumentos antes de pressionar a tecla Enter. Normalmente, as opções alteram o comportamento do comando e os argumentos são itens ou valores para o comando agir.

O comando ``` pwd ``` pode ser usado para mostras sua localização atual dentro de um sistema de arquivos.

Use o comando ``` cd ``` para alterar diretórios.
    cd [opções] [caminho]

### Argumentos
Um argumento pode ser usado para especificar algo para o comando agir. O comando ``` ls ``` pode ser dado o nome de um diretório como um argumento, e ele irá listar o conteúdo desse diretório.

Como o Linux é de código aberto, existem alguns segredos interessantes que foram adicionados pelos desenvolvedores, pesquise-os para saber mais!

### Opções
As opções podem ser usadas para alterar o comportamento de um comando. O comando ``` ls ``` foi usado para listar o conteúdo de um diretório e a opção ``` -l ``` resulta em uma saída de "exibição longa", ou seja, fornece mais irformações sobre cada um dos arquivos listados.

Muitas vezes, o caractere é escolhido para ser mnemônico para o seu propósito, como escolher a letra "l" para longo ou "r" para reverso. Por padrão o comando ``` ls ``` imprime os resultados em ordem alfabética, se adicionarmos a opção ``` -r ``` irá imprimir os resultados em ordem alfabética inversa.

As opções podem ser usadas de uma só vez, por exemplo ``` ls -l -r ``` ou ``` ls -rl ``` ou ``` ls -lr ```. Todas as opções vão gerar o mesmo resultado.