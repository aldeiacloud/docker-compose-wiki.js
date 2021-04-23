<b>RESUMO:</b><br>Configuração da Wiki.js em Ubuntu 18.04/20.04.

<b>Vídeo da implementação: https://www.youtube.com/watch</b>

------------------------------------------------------------------------------

<b>1- </b>Subir instância EC2 com Ubuntu 18.04 ou 20.04.

------------------------------------------------------------------------------

<b>2- </b>Atachar IP na instância.

------------------------------------------------------------------------------

<b>3- </b>Apontar um subdominio para o IP da instância na tabela de DNS. (Ex.: wiki.aldeiacloud.com.br)

------------------------------------------------------------------------------

<b>4- </b>Logar na instância e atualizar a lista de repositórios. <br>apt update

------------------------------------------------------------------------------

<b>5- </b>Instalar docker-compose e git. <br>sudo apt install docker-compose -y && sudo apt install git -y

------------------------------------------------------------------------------

<b>6- </b> Clonar repositório. <br>git clone https://github.com/aldeiacloud/docker-compose-wiki.js.git

------------------------------------------------------------------------------

<b>7- </b> Entrar no diretório "/nginx/ssl/" e depois usar o seguinte comando para solicitar os certificados.<br>
openssl req -new -newkey rsa:2048 -nodes -keyout privkey.key -out solicitacao.csr

------------------------------------------------------------------------------

<b>8- </b> Abrir gogetssl e solicitar um certificado gratuito e adiciona-lo dentro de "/nginx/ssl/"

------------------------------------------------------------------------------

<b>9- </b> Subir o container.<br>~~docker-compose up -d~~
