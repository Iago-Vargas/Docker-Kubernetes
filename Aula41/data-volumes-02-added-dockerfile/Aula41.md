# VOLUME em DockerFile
## Volume com nome ANONIMO
- Instrucao onde mostramos quais dados devem ser persistentes, informa ao docker que arquivos criados em /xyz/xyz devem dizer em um volume gerenciado pelo Docker
   - VOLUME [ "/xyz/xyz" ]
- O VOLUME não copia arquivos para uma pasta do meu computador e não define nomes. Ele marca apenas o diretorio como ponto de volume desse conteiner, o nome é escolhido pelo Docker Run no Docker Compose
- É mais boa pratica definir o VOLUME no Docker Compose
- Se definirmos com nome anonimo ele vai subir com nosso conteiner e o mesmo vai autogerar um nome a ele, com isso ao fechar o conteiner todas informacoes que estao dentro do VOLUME vao ser apagadas e refeitas

## Volume com nome DEFINIDO
- Para definirmos um nome no VOLUME iremos retirar da DockerFile o VOLUME [ "/xyz/xyz" ] e iremos subir da seguinte maneira
  - docker run --name <nomeConteiner> -v <nomeVolume>:<caminhoVolume> <imagem>
- Dessa forma vamos determinar caminho e nome ao Volume e por mais que pare e suba novamente o conteiner ele vai seguir com seus dados guardados
- Para verificar o nome do VOLUME rodamos
  - docker volume ls
  