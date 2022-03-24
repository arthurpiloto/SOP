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