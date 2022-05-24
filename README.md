# rclone
Na intenção de automatizar o backup de arquivos do meu computador linux para o google drive configurei o rclone para fazer essa tarefa automaticamente.


Segue tutorial de instalação do rclone no ubuntu: (Precisa estar logado como root)

Para instalar o rclone no linux basta seguir esse passo a passo:

1- wget https://downloads.rclone.org/rclone-current-linux-amd64.deb
2- sudo dpkg -i rclone-current-linux-amd64.deb

Depois iniciamos a configuração do rclone:

1- rclone config


No remotes found - make a new one
n) New remote
s) Set configuration password
q) Quit config
n/s/q>  N

name> nome que deseja utilizar no comando rclone para referenciar o serviço de nuvem utlizado, por exemplo 'gdrive';

na sequencia devem ser mostrados os serviços de nuvem que podem ser utlizados, no meu caso como estou usando o google drive, selecionei '15':

15 / Google Drive
   \ "drive"

client_id> SÓ CLICAR EM ENTER PARA CONTINUAR

client_secret> SÓ CLICAR EM ENTER PARA CONTINUAR


Scope that rclone should use when requesting access from drive.
Enter a string value. Press Enter for the default ("").
Choose a number from below, or type in your own value

nesse caso selecione a opção 1:

 1 / Full access all files, excluding Application Data Folder.
   \ "drive"

root_folder_id> SÓ CLICAR EM ENTER PARA CONTINUAR

Enter a string value. Press Enter for the default ("").
service_account_file > SÓ CLICAR EM ENTER PARA CONTINUAR


Edit advanced config?
y) Yes
n) No (default)
y/n> n


use auto config ? YES


Em seguida abrirá uma página do navegador para fazer login na conta do google (ou outro serviço que você esteja configurando) e permitir o acesso do rclone;

Depois é só rodar o comando do script e backup que deixei junto nesse repositório.
