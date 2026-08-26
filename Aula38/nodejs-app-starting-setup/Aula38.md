# Versionamento com Docker Hub
- Passos que fizemos foi criar um repositorio virtual no Docker Hub
  - Ao criar esse repositorio viemos para nossa plataforma e rodamos:
    - docker images 
    - Localizamos a imagem que gostariamos de colocar na nuvem
  - Ao pegar essa imagem vamos rodar o seguinte comando
    - docker tag <imagem:quevaisubir> <nome/repositorionuvem>
  - Apos a execucao desse comando vamos ver em docker images que temos a nova imagem e a antiga na nossa listagem, para enviar a nuvem usamos
    - docker push <nome/repositorio>
  - Assim ao entrar no DockerHub vamos verificar que nossa imagem já esta la na Nuvem.