# VOLUME em DockerFile
- Instrucao onde mostramos quais dados devem ser persistentes, informa ao docker que arquivos criados em /xyz/xyz devem dizer em um volume gerenciado pelo Docker
   - VOLUME [ "/xyz/xyz" ]
- O VOLUME não copia arquivos para uma pasta do meu computador e não define nomes. Ele marca apenas o diretorio como ponto de volume desse conteiner, o nome é escolhido pelo Docker Run no Docker Compose
- É mais boa pratica definir o VOLUME no Docker Compose