# Nginx Proxy Manager com Docker Compose

Este projeto configura um Nginx Proxy Manager usando Docker Compose. O Nginx Proxy Manager é uma solução fácil de usar para gerenciar proxies reversos e certificados SSL em uma interface web intuitiva.

## Pré-requisitos

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [MySQL](https://www.mysql.com/)

## Estrutura do Projeto

Este projeto inclui um arquivo `docker-compose.yml` para orquestrar os serviços necessários para rodar o Nginx Proxy Manager. 

## Como Usar

1. **Clone o Repositório**

   Clone este repositório para o seu ambiente local:

 ```bash
 git clone git@github.com:pedroinbezerra/nginx-proxy-manager.git
 cd nginx-proxy-manager
 ```
Configuração do Docker Compose

Certifique-se de que o Docker e o Docker Compose estão instalados em seu sistema. Em seguida, edite o arquivo docker-compose.yml se necessário para ajustar as configurações.

A configuração do banco de dados deve ser realizada no arquivo `.env`. Você pode usar o arquivo `.env.example` como ponto de partida. As variáveis de ambiente devem ser configuradas da seguinte forma:

```env
DB_MYSQL_HOST=localhost
DB_MYSQL_PORT=3306
DB_MYSQL_USER=nginx
DB_MYSQL_PASSWORD=nginx
DB_MYSQL_NAME=nginx
```

Executar os Contêineres

Execute o Docker Compose para iniciar os contêineres:

```bash
docker-compose up -d
```

O parâmetro -d faz com que os contêineres sejam executados em segundo plano.

Acessar a Interface Web

Após a execução bem-sucedida dos contêineres, você pode acessar a interface web do Nginx Proxy Manager em:

```
http://<SEU_IP>:81
```

Por padrão, o Nginx Proxy Manager está configurado para escutar na porta 81.

Credenciais de Login

As credenciais padrão para o Nginx Proxy Manager são:

```
E-mail: admin@example.com
Senha: changeme
```

Nota: Recomendo fortemente que você altere estas credenciais após o primeiro login.

Configuração Adicional
Você pode ajustar as configurações do Nginx Proxy Manager editando o arquivo docker-compose.yml. Para mais informações sobre as opções de configuração, consulte a documentação oficial do [Nginx Proxy Manager](https://nginxproxymanager.com/).
