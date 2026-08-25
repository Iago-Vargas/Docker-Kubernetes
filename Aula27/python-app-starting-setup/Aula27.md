# Modo Interativo
- Quando estamos executando um codigo que somente possui uma saida via terminal, precisamos que o mesmo seja interativo pois depende de respostar, por isso utilizamos:
- docker run -it {nome} - Dessa forma nosso conteiner vai subir de forma interativa, conseguindo assim inserir valores e interagir com o terminal.
- docker start -a -t {nome} - Subimos o conteiner que estava pausado de forma interativa e attached o mesmo, fazendo assim com que ele escute e grave no terminal.