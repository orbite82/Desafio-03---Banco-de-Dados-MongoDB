<div align="center">
<img src="https://user-images.githubusercontent.com/47891196/139104117-aa9c2943-37da-4534-a584-e4e5ff5bf69a.png" width="350px" />
</div>

# Desafio 03 - Banco de Dados MongoDB

Para criar um contêiner do MongoDB com as especificações que você mencionou, você pode usar o Docker. Aqui está um comando simples que você pode executar para criar o contêiner:

```bash
docker run -d \
  --name mongodb \
  -e MONGO_INITDB_ROOT_USERNAME=mongo_usr \
  -e MONGO_INITDB_ROOT_PASSWORD=mongo_pwd \
  -p 27017:27017 \
  mongo
```

### Explicação dos parâmetros:

- `docker run -d`: Executa o contêiner em segundo plano (modo "detached").
- `--name mongodb`: Nomeia o contêiner de "mongodb".
- `-e MONGO_INITDB_ROOT_USERNAME=mongo_usr`: Define o nome de usuário do root como "mongo_usr".
- `-e MONGO_INITDB_ROOT_PASSWORD=mongo_pwd`: Define a senha do root como "mongo_pwd".
- `-p 27017:27017`: Mapeia a porta padrão do MongoDB (27017) do contêiner para a máquina host.
- `mongo`: Indica a imagem do MongoDB a ser utilizada.

### Acessando o MongoDB

Após iniciar o contêiner, você pode acessar o MongoDB usando um cliente, como o MongoDB Shell ou uma interface gráfica. Para se conectar, use:

```bash
mongo -u mongo_usr -p mongo_pwd --authenticationDatabase admin
```

### Parando e removendo o contêiner

Se precisar parar ou remover o contêiner, você pode usar os seguintes comandos:

- Para parar o contêiner:
  ```bash
  docker stop mongodb
  ```

- Para remover o contêiner:
  ```bash
  docker rm mongodb
  ```

Certifique-se de ter o Docker instalado e em funcionamento no seu sistema antes de executar esses comandos! Se precisar de mais alguma coisa, é só avisar.
