# VOLUME no Dockerfile

## Volume anônimo

- A instrução `VOLUME` indica que determinado diretório do container deve armazenar dados em um volume gerenciado pelo Docker.

  ```dockerfile
  VOLUME ["/xyz/xyz"]
  ```

- O `VOLUME` não copia os arquivos para uma pasta específica do computador e não define o nome do volume. Ele apenas marca o diretório como um ponto de montagem.
- Se não informarmos um volume no `docker run` ou no Docker Compose, o Docker cria automaticamente um volume anônimo, com um nome aleatório.
- O volume anônimo não é apagado quando o container é apenas parado.
- Se o container for removido e outro for criado, um novo volume anônimo poderá ser gerado. O volume anterior continuará existindo, mas não será conectado automaticamente ao novo container.
- Um volume pode ser removido junto com o container ao utilizarmos:

  ```bash
  docker run --rm <imagem>
  ```

  ou:

  ```bash
  docker rm -v <nome-container>
  ```

- Para remover volumes que não estão sendo utilizados:

  ```bash
  docker volume prune
  ```

- Geralmente, é mais prático declarar os volumes no Docker Compose, pois a configuração fica mais explícita.

## Volume nomeado

- Não é necessário retirar a instrução `VOLUME` do Dockerfile para utilizar um volume nomeado.
- Podemos definir o nome do volume ao criar o container:

  ```bash
  docker run --name <nome-container> -v <nome-volume>:<caminho-no-container> <imagem>
  ```

- Exemplo:

  ```bash
  docker run --name feedback-app -v feedback-data:/app/feedback minha-imagem
  ```

- Nesse exemplo, o volume `feedback-data` será montado no diretório `/app/feedback` do container.
- Mesmo que o container seja parado ou removido, os dados continuarão armazenados no volume. Para recuperá-los, basta montar o mesmo volume em outro container.
- Para listar os volumes existentes:

  ```bash
  docker volume ls
  ```

## Resumo

- `docker stop`: o container e o volume continuam existindo.
- `docker rm`: remove o container, mas normalmente não remove o volume.
- Um novo container com volume anônimo normalmente recebe um novo volume.
- Um novo container usando o mesmo volume nomeado recupera os dados anteriores.
